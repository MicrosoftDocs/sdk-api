---
UID: NF:oleauto.VarNumFromParseNum
title: VarNumFromParseNum function (oleauto.h)
description: Converts parsed results to a variant.
helpviewer_keywords: ["VTBIT_CY","VTBIT_DECIMAL","VTBIT_I1","VTBIT_I2","VTBIT_I4","VTBIT_R4","VTBIT_R8","VTBIT_UI1","VTBIT_UI2","VTBIT_UI4","VarNumFromParseNum","VarNumFromParseNum function [Automation]","_oa96_VarNumFromParseNum","automat.varnumfromparsenum","oleauto/VarNumFromParseNum"]
old-location: automat\varnumfromparsenum.htm
tech.root: automat
ms.assetid: 6a01a779-ab1b-4fd5-a550-449b19358b7a
ms.date: 12/05/2018
ms.keywords: VTBIT_CY, VTBIT_DECIMAL, VTBIT_I1, VTBIT_I2, VTBIT_I4, VTBIT_R4, VTBIT_R8, VTBIT_UI1, VTBIT_UI2, VTBIT_UI4, VarNumFromParseNum, VarNumFromParseNum function [Automation], _oa96_VarNumFromParseNum, automat.varnumfromparsenum, oleauto/VarNumFromParseNum
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarNumFromParseNum
 - oleauto/VarNumFromParseNum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarNumFromParseNum
---

# VarNumFromParseNum function


## -description

Converts parsed results to a variant.

## -parameters

### -param pnumprs [in]

The parsed results. The <b>cDig</b> member of this argument specifies the number of digits present in <i>rgbDig</i>.

### -param rgbDig [in]

The values of the digits. The <b>cDig</b> field of <i>pnumprs</i> contains the number of digits.

### -param dwVtBits [in]

One bit set for each type that is acceptable as a return value (in many cases, just one bit).

<a id="VTBIT_I1"></a>
<a id="vtbit_i1"></a>


#### VTBIT_I1

<a id="VTBIT_UI1"></a>
<a id="vtbit_ui1"></a>


#### VTBIT_UI1

<a id="VTBIT_I2"></a>
<a id="vtbit_i2"></a>


#### VTBIT_I2

<a id="VTBIT_UI2"></a>
<a id="vtbit_ui2"></a>


#### VTBIT_UI2

<a id="VTBIT_I4"></a>
<a id="vtbit_i4"></a>


#### VTBIT_I4

<a id="VTBIT_UI4"></a>
<a id="vtbit_ui4"></a>


#### VTBIT_UI4

<a id="VTBIT_R4"></a>
<a id="vtbit_r4"></a>


#### VTBIT_R4

<a id="VTBIT_R8"></a>
<a id="vtbit_r8"></a>


#### VTBIT_R8

<a id="VTBIT_CY"></a>
<a id="vtbit_cy"></a>


#### VTBIT_CY

<a id="VTBIT_DECIMAL"></a>
<a id="vtbit_decimal"></a>


#### VTBIT_DECIMAL

### -param pvar [out]

The variant result.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The number is too large to be represented in an allowed type. There is no error if precision is lost in the conversion.


</td>
</tr>
</table>

## -remarks

For rounding decimal numbers, the digit array must be at least one digit longer than the maximum required for data types. The maximum number of digits required for the DECIMAL data type is 29, so the digit array must have room for 30 digits. There must also be enough digits to accept the number in octal, if that parsing options is selected. (Hexadecimal and octal numbers are limited by <b>VarNumFromParseNum</b> to the magnitude of an unsigned long [32 bits], so they need 11 octal digits.)

