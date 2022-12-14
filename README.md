# T41-ML-brocolli
Experimental hyperoptimization of different crypto trading strategies

## BrocolliV1
BrocolloV1 is the first strategy we created just to see how to operate freqtrade, EMA (exponential moving average) is flipped, short and long entries are hyperoptable using freqtrade's in-built hyperopt library (uses `scikit-optimize` under the hood)

## BrocolliBB
Bollinger bands help understand patterns and relative strength index supports it. Bollinger bands are defined by two standard deviation difference (one positive, one negative) from a simple moving average (SMA). In the historical charts below, Bollinger are a reliable indicator of a crypto's volatility. It's been a pretty good metric and this strategy combines it with the simple RSI

## BrocolliV2
This strategy was implemented with more vanilla technical indicators such as EMA. Checks that attempt to determine whether a crypto trading pair is risky (low liquidity) are also done and unreliable pairs are not bought into.


# Strategy comparison

We also did a "literature review" and compared how other state-of-the-art hyperoptable trading strategies (under review_strategies) compare with ours. Surprise, surprise.. they faired much better in backtests and live.


For hyperopting to most recent trends:

`freqtrade hyperopt --hyperopt-loss SortinoHyperOptLoss --spaces buy sell --strategy {HYPEROPT_LOSS} --timerange 20220125- -j 2 -e 200`


