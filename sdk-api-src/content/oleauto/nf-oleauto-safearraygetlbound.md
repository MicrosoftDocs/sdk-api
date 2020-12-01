---
UID: NF:oleauto.SafeArrayGetLBound
title: SafeArrayGetLBound function (oleauto.h)
description: Gets the lower bound for any dimension of the specified safe array.
helpviewer_keywords: ["SafeArrayGetLBound","SafeArrayGetLBound function [Automation]","_oa96_SafeArrayGetLBound","automat.safearraygetlbound","oleauto/SafeArrayGetLBound"]
old-location: automat\safearraygetlbound.htm
tech.root: automat
ms.assetid: f3134cc9-759b-4908-ada0-d025a525e795
ms.date: 12/05/2018
ms.keywords: SafeArrayGetLBound, SafeArrayGetLBound function [Automation], _oa96_SafeArrayGetLBound, automat.safearraygetlbound, oleauto/SafeArrayGetLBound
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
 - SafeArrayGetLBound
 - oleauto/SafeArrayGetLBound
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
 - SafeArrayGetLBound
---

# SafeArrayGetLBound function


## -description

Gets the lower bound for any dimension of the specified safe array.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

### -param nDim [in]

The array dimension for which to get the lower bound.

### -param plLbound [out]

The lower bound.

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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified index is out of bounds.

</td>
</tr>
</table>