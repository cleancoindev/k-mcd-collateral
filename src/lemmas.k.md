```k
rule (X *Int pow176 +Int (Y *Int pow168 +Int Z *Int pow160 +Int A)) /Int pow160 => X *Int pow16 +Int (Y *Int pow8 +Int Z)
  requires #rangeUInt(8, X)
  andBool #rangeUInt(8, Y)
  andBool #rangeUInt(8, Z)
  andBool #rangeAddress(A)

rule 255 &Int (X *Int pow16 +Int (Y *Int pow8 +Int Z)) => Z
  requires #rangeUInt(8, X)
  andBool #rangeUInt(8, Y)
  andBool #rangeUInt(8, Z)

rule (X *Int pow176 +Int (Y *Int pow168 +Int A)) /Int pow160 => X *Int pow16 +Int Y *Int pow8
  requires #rangeUInt(8, X)
  andBool  #rangeUInt(8, Y)
  andBool  #rangeAddress(A)

rule 255 &Int (X *Int pow16 +Int Y *Int pow8) => 0
  requires #rangeUInt(8, X)
  andBool  #rangeUInt(8, Y)
```
