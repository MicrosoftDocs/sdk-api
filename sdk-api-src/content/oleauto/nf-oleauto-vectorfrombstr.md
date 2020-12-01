---
UID: NF:oleauto.VectorFromBstr
title: VectorFromBstr function (oleauto.h)
description: Returns a vector, assigning each character in the BSTR to an element of the vector.
helpviewer_keywords: ["VectorFromBstr","VectorFromBstr function [Automation]","_oa96_VectorFromBstr","automat.vectorfrombstr","oleauto/VectorFromBstr"]
old-location: automat\vectorfrombstr.htm
tech.root: automat
ms.assetid: 46cde8da-f6c8-4b29-b4ef-eda30b0fa3f1
ms.date: 12/05/2018
ms.keywords: VectorFromBstr, VectorFromBstr function [Automation], _oa96_VectorFromBstr, automat.vectorfrombstr, oleauto/VectorFromBstr
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
 - VectorFromBstr
 - oleauto/VectorFromBstr
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
 - VectorFromBstr
---

# VectorFromBstr function


## -description

Returns a vector, assigning each character in the BSTR to an element of the vector.

## -parameters

### -param bstr [in]

The BSTR to be converted to a vector.

### -param ppsa [out]

A one-dimensional safearray containing the characters in the BSTR.

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
The <i>bstr</i> parameter is null.


</td>
</tr>
</table>

