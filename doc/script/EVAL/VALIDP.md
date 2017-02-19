# EVAL/VALID?

Assesses validity of the code from the perspective of decoding

Input stack: `code`

Output stack: `1` or `0`

`EVAL/VALID?` will only verify if PumpkinDB will be able to
interpret the code. However, it won't assess any other properties
pertaining to its validity.

Generally speaking, this word is only reserved for
some special cases as `EVAL` will fail upon trying to
evaluate incorrect code anyway.

## Allocation

Allocates for parsing the binary representation of the program.

## Errors

[EmptyStack](./ERRORS/EmptyStack.md) error if there is less than
one item on the stack

## Examples

```
1 EVAL/VALID? => 0x00
'DUP EVAL/VALID? => 0x01
[1 DUP] EVAL/VALID? => 0x01
```

## Tests

```
1 EVAL/VALID? => 0x00
'DUP EVAL/VALID? => 0x01
[1 DUP] EVAL/VALID? => 0x01
```