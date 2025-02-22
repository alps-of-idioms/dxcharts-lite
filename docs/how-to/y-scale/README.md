# Y-Axis

#### <!--CSB_LINK-->[Live Example](https://codesandbox.io/s/g76qzp)<!--/CSB_LINK-->

Scale presentation can be controlled using following API

## Visibility

Hides the axis, does not change the width, just hides prices

```js
chartInstance.yAxisComponent.setVisible(true))
```

## Inversion

Reverts the axis and candles top to bottom

```js
chartInstance.yAxisComponent.togglePriceScaleInverse(true);
chartInstance.redraw();
```

## setLockPriceToBarRatio

Keeps the ratio between `y` and `x` axes constant on zoom
wont work on percent or logarithmic scale

```js
chartInstance.yAxisComponent.setLockPriceToBarRatio(true);
```

## Axis alignment

Defines the axis' placement, to the `left` or `right` of the candles

```js
chartInstance.yAxisComponent.setYAxisAlign('right' /*'left'*/);
```

## Axis type

There are 3 different modes of scaling

-   `regular` - linear scale, set in prices equidistant from each other
-   `logarithmic` - a base 2 logarithm scale in prices
-   `percent` - renders scale in percentage from the first visible candle's closing price
    chart is not manually scalable in percentage mode, only shift on the x-axis is allowed

```js
chartInstance.yAxisComponent.setAxisType('regular' /*'logarithmic' 'percent'*/);
```

<iframe src="./index.html" style="width:100%; border:none; height: 310px" title="DXCharts Lite React integration"></iframe>
