# phpdicecalc

----

A simple infix to RPN converter and calculator, supporting dice and set notation.

## How to use?
```php
// Set the expression
$expression = '4+5';

// Create the Calc object with the expression
$calc = new Calc($expression);

// Output the expresison
echo "{$expression}\n";

// Output the infix interpretation and the calculation
echo $calc->infix() . " = " . $calc->calc() . "\n";
```


## Supported Dice Notation
There's probably some BNF that would describe this best, but until then, some examples:

## Simple Examples
* 1d4 = Roll a four-sided die once.
* 3d6 = Roll three six-sided dice.
* 2d10 = Roll two ten-sided dice.
* d20 = Roll a twenty-sided die once.
* d% = Roll a 100-sided die once.

##Examples with Modifiers
* 4d6 keep > 2 = Roll 4d6, keep only those dice with a value higher than 2
* 2d8 keep < 6 = Roll 2d8, keep only those dice with a value less than 6
* 6d10 keep > 5 = Roll 6d10, keep only those dice * with a value greater than 5 (White Wolf-style)
* 3d6 reroll < 3 = Roll 3d6, reroll any value less than 3
* 2s20 reroll > 15 = Roll 2d20, reroll any value greater than 15
* 4d6 highest 3 = Roll 4d6, keep only the highest 3 values
* 4d6 lowest 3 = Roll 4d6, keep only the lowest 3 values
* 4d6 reroll < 3 highest 3 = Roll 3d6, reroll any value less than 3, keep only the highest 3 values
* 4[d6 open = 6] > 7 = Roll 4d6. Re-roll any die that comes up 6, adding the result, and repeat this process until the re-roll isn't a 6. If any of the results are greater than 7, return true, otherwise false. (Shadowrun-style)

----
## Thanks
* [phpdicecalc](https://code.google.com/p/phpdicecalc/)

I really appreciate for someone who made this code, unfortunately this code is still on google project, and the owner of this code is doesn't care that Google Code will be shut down, so before Google Code shut down, i copied this code to Github
