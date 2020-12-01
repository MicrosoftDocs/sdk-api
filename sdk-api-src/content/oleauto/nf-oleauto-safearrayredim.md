---
UID: NF:oleauto.SafeArrayRedim
title: SafeArrayRedim function (oleauto.h)
description: Changes the right-most (least significant) bound of the specified safe array.
helpviewer_keywords: ["SafeArrayRedim","SafeArrayRedim function [Automation]","_oa96_SafeArrayRedim","automat.safearrayredim","oleauto/SafeArrayRedim"]
old-location: automat\safearrayredim.htm
tech.root: automat
ms.assetid: 1c7fa627-e5e4-4bb9-8237-2f7358ebc4b8
ms.date: 12/05/2018
ms.keywords: SafeArrayRedim, SafeArrayRedim function [Automation], _oa96_SafeArrayRedim, automat.safearrayredim, oleauto/SafeArrayRedim
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
 - SafeArrayRedim
 - oleauto/SafeArrayRedim
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
 - SafeArrayRedim
---

# SafeArrayRedim function


## -description

Changes the right-most (least significant) bound of the specified safe array.

## -parameters

### -param psa [in, out]

A safe array descriptor.

### -param psaboundNew [in]

A new safe array bound structure that contains the new array boundary. You can change only the least significant dimension of an array.

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
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The array is locked.

</td>
</tr>
</table>

## -remarks

If you reduce the bound of an array, <b>SafeArrayRedim</b> deallocates the array elements outside the new array boundary. If the bound of an array is increased, <b>SafeArrayRedim</b> allocates and initializes the new array elements. The data is preserved for elements that exist in both the old and new array.

