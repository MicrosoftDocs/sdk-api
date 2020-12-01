---
UID: NF:oleauto.VarI8FromBool
title: VarI8FromBool function (oleauto.h)
description: Converts a Boolean value to an 8-byte integer value.
helpviewer_keywords: ["VarI8FromBool","VarI8FromBool function [Automation]","_oa96_VarI8FromBool","automat.vari8frombool","oleauto/VarI8FromBool"]
old-location: automat\vari8frombool.htm
tech.root: automat
ms.assetid: 5de56332-2e1c-444d-af14-3d217cd4494a
ms.date: 12/05/2018
ms.keywords: VarI8FromBool, VarI8FromBool function [Automation], _oa96_VarI8FromBool, automat.vari8frombool, oleauto/VarI8FromBool
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
 - VarI8FromBool
 - oleauto/VarI8FromBool
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
 - VarI8FromBool
---

# VarI8FromBool function


## -description

Converts a Boolean value to an 8-byte integer value.

## -parameters

### -param boolIn [in]

The value to convert.

### -param pi64Out [out]

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

