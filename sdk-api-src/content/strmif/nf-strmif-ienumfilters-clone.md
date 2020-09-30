---
UID: NF:strmif.IEnumFilters.Clone
title: IEnumFilters::Clone (strmif.h)
description: The Clone method makes a copy of the enumerator object. The returned object starts with the same enumeration state as the original.
helpviewer_keywords: ["Clone","Clone method [DirectShow]","Clone method [DirectShow]","IEnumFilters interface","IEnumFilters interface [DirectShow]","Clone method","IEnumFilters.Clone","IEnumFilters::Clone","IEnumFiltersClone","dshow.ienumfilters_clone","strmif/IEnumFilters::Clone"]
old-location: dshow\ienumfilters_clone.htm
tech.root: dshow
ms.assetid: ed8380af-8467-447a-a595-38fe29f9f9e6
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumFilters interface, IEnumFilters interface [DirectShow],Clone method, IEnumFilters.Clone, IEnumFilters::Clone, IEnumFiltersClone, dshow.ienumfilters_clone, strmif/IEnumFilters::Clone
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumFilters::Clone
 - strmif/IEnumFilters::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumFilters.Clone
---

# IEnumFilters::Clone


## -description

The <code>Clone</code> method makes a copy of the enumerator object. The returned object starts with the same enumeration state as the original.

## -parameters

### -param ppEnum [out]

Receives a pointer to the <b>IEnumFilters</b> interface of the new enumerator. The caller must release the interface.

## -returns

Returns one of the following <b>HRESULTs</b>.

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
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumfilters">IEnumFilters Interface</a>