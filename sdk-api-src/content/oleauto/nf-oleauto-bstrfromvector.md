---
UID: NF:oleauto.BstrFromVector
title: BstrFromVector function (oleauto.h)
description: Returns a BSTR, assigning each element of the vector to a character in the BSTR.
helpviewer_keywords: ["BstrFromVector","BstrFromVector function [Automation]","_oa96_BstrFromVector","automat.bstrfromvector","oleauto/BstrFromVector"]
old-location: automat\bstrfromvector.htm
tech.root: automat
ms.assetid: 26955616-698b-4f63-b652-af7dfaa23e43
ms.date: 12/05/2018
ms.keywords: BstrFromVector, BstrFromVector function [Automation], _oa96_BstrFromVector, automat.bstrfromvector, oleauto/BstrFromVector
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
 - BstrFromVector
 - oleauto/BstrFromVector
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
 - BstrFromVector
---

# BstrFromVector function


## -description

Returns a BSTR, assigning each element of the vector to a character in the BSTR.

## -parameters

### -param psa [in]

The vector to be converted to a BSTR.

### -param pbstr [out]

A BSTR, each character of which is assigned to an element from the vector.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>psa</i> parameter is null.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH
</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> is not a vector (not an array of bytes).


</td>
</tr>
</table>

