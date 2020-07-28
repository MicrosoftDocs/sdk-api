---
UID: NF:oleauto.VarR4FromDec
title: VarR4FromDec function (oleauto.h)
description: Converts a decimal value to a float value.
helpviewer_keywords: ["VarR4FromDec","VarR4FromDec function [Automation]","_oa96_VarR4FromDec","automat.varr4fromdec","oleauto/VarR4FromDec"]
old-location: automat\varr4fromdec.htm
tech.root: automat
ms.assetid: d8cee8c9-fe6c-4470-a3a7-00ffbc07d2c0
ms.date: 12/05/2018
ms.keywords: VarR4FromDec, VarR4FromDec function [Automation], _oa96_VarR4FromDec, automat.varr4fromdec, oleauto/VarR4FromDec
f1_keywords:
- oleauto/VarR4FromDec
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
- VarR4FromDec
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarR4FromDec function


## -description


Converts a decimal value to a float value.


## -parameters




### -param pdecIn [in]

The value to convert.


### -param pfltOut [out]

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
 



