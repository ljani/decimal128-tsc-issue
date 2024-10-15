# decimal128-tsc-issue

Steps:

- Run `npm run build`

Expected result:

- Build completes successfully

Actual result:

- Build fails:
    ```text
    node_modules/decimal128/src/Decimal.mts:3:7 - error TS6133: 'ratOne' is declared but its value is never read.

    3 const ratOne = new Rational(1n, 1n);
            ~~~~~~

    node_modules/decimal128/src/Decimal.mts:4:7 - error TS6133: 'ratTen' is declared but its value is never read.

    4 const ratTen = new Rational(10n, 1n);
            ~~~~~~

    node_modules/decimal128/src/Decimal.mts:49:14 - error TS6133: 'dec' is declared but its value is never read.

    49         let [dec, exp] = s.split(/[eE]/);
                    ~~~

    node_modules/decimal128/src/Decimal128.mts:45:5 - error TS6133: 'd' is declared but its value is never read.

    45     d: "0" | "-0" | Rational,
           ~

    node_modules/decimal128/src/Rational.mts:7:5 - error TS6133: 'ROUNDING_MODE_HALF_EXPAND' is declared but its value is never read.

    7     ROUNDING_MODE_HALF_EXPAND,
          ~~~~~~~~~~~~~~~~~~~~~~~~~

    node_modules/decimal128/src/Rational.mts:321:9 - error TS6133: 'penultimateDigit' is declared but its value is never read.

    321         penultimateDigit: Digit,
                ~~~~~~~~~~~~~~~~

    node_modules/decimal128/src/Rational.mts:337:9 - error TS6133: 'penultimateDigit' is declared but its value is never read.

    337         penultimateDigit: Digit,
                ~~~~~~~~~~~~~~~~

    node_modules/decimal128/src/Rational.mts:354:9 - error TS6133: 'penultimateDigit' is declared but its value is never read.

    354         penultimateDigit: Digit,
                ~~~~~~~~~~~~~~~~

    node_modules/decimal128/src/Rational.mts:355:9 - error TS6133: 'finalDigit' is declared but its value is never read.

    355         finalDigit: Digit,
                ~~~~~~~~~~


    Found 9 errors.
```
