---
UID: NF:oleauto.VarUI1FromDec
title: VarUI1FromDec function (oleauto.h)
description: Converts a decimal value to an unsigned char value.helpviewer_keywords: ["VarUI1FromDec","VarUI1FromDec function [Automation]","_oa96_VarUI1FromDec","automat.varui1fromdec","oleauto/VarUI1FromDec"]
old-location: automat\varui1fromdec.htm
tech.root: automat
ms.assetid: 9a8a8403-473e-47da-a7ee-11568ae1588f
ms.date: 12/05/2018
ms.keywords: VarUI1FromDec, VarUI1FromDec function [Automation], _oa96_VarUI1FromDec, automat.varui1fromdec, oleauto/VarUI1FromDec
f1_keywords:
- oleauto/VarUI1FromDec
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarUI1FromDec
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarUI1FromDec function


## -description


Converts a decimal value to an unsigned char value.


## -parameters




### -param pdecIn [in]

The value to convert.


### -param pbOut [out]

The resulting value.


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
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by the output parameter does not fit in the destination type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 



