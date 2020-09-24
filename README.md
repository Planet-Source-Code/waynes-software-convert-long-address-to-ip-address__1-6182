<div align="center">

## Convert long address to IP address


</div>

### Description

Converts a long address (2220112843) to it's IP address (203.59.84.132)
 
### More Info
 
Example:

Result = IPToString(2220112843#)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Waynes Software](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/waynes-software.md)
**Level**          |Intermediate
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__1-5.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/waynes-software-convert-long-address-to-ip-address__1-6182/archive/master.zip)

### API Declarations

```
Type MyLong
  Value As Long
End Type
Type MyIP
  A As Byte
  B As Byte
  C As Byte
  D As Byte
End Type
```


### Source Code

```
Function IPToString(Value As Double) As String
  Dim l As MyLong
  Dim i As MyIP
  l.Value = DoubleToLong(Value)
  LSet i = l
  IPToString = i.A & "." & i.B & "." & i.C & "." & i.D
End Function
Function DoubleToLong(Value As Double) As Long
  If Value <= 2147483647 Then
    DoubleToLong = Value
  Else
    DoubleToLong = -(4294967296# - Value)
  End If
End Function
```

