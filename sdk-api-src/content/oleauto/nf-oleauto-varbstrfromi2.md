---
UID: NF:oleauto.VarBstrFromI2
title: VarBstrFromI2 function (oleauto.h)
description: Converts a short value to a BSTR value.
helpviewer_keywords: ["VarBstrFromI2","VarBstrFromI2 function [Automation]","_oa96_VarBstrFromI2","automat.varbstrfromi2","oleauto/VarBstrFromI2"]
old-location: automat\varbstrfromi2.htm
tech.root: automat
ms.assetid: 0c9051f9-1c2f-4882-bff9-7d28440dd06d
ms.date: 12/05/2018
ms.keywords: VarBstrFromI2, VarBstrFromI2 function [Automation], _oa96_VarBstrFromI2, automat.varbstrfromi2, oleauto/VarBstrFromI2
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
 - VarBstrFromI2
 - oleauto/VarBstrFromI2
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
 - VarBstrFromI2
---

# VarBstrFromI2 function


## -description

Converts a short value to a BSTR value.

## -parameters

### -param iVal [in]

The value to convert.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

Reserved. Set to zero.

### -param pbstrOut

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

