---
UID: NF:bdaiface.IEnumPIDMap.Clone
title: IEnumPIDMap::Clone (bdaiface.h)
description: The Clone method creates a copy the collection.
helpviewer_keywords: ["Clone","Clone method [DirectShow]","Clone method [DirectShow]","IEnumPIDMap interface","IEnumPIDMap interface [DirectShow]","Clone method","IEnumPIDMap.Clone","IEnumPIDMap::Clone","IEnumPIDMapClone","bdaiface/IEnumPIDMap::Clone","dshow.ienumpidmap_clone"]
old-location: dshow\ienumpidmap_clone.htm
tech.root: dshow
ms.assetid: 4d965a71-ff5e-4d4a-8976-0de5b8bbae04
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumPIDMap interface, IEnumPIDMap interface [DirectShow],Clone method, IEnumPIDMap.Clone, IEnumPIDMap::Clone, IEnumPIDMapClone, bdaiface/IEnumPIDMap::Clone, dshow.ienumpidmap_clone
req.header: bdaiface.h
req.include-header: 
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
 - IEnumPIDMap::Clone
 - bdaiface/IEnumPIDMap::Clone
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
 - IEnumPIDMap.Clone
---

# IEnumPIDMap::Clone


## -description

The <code>Clone</code> method creates a copy the collection.

## -parameters

### -param ppIEnumPIDMap [out]

Receives an <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap</a> interface pointer, representing the new collection. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>ppIEnumPIDMap</i> cannot be <b>NULL</b>.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The caller must release the returned <b>IEnumPIDMap</b> interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap Interface</a>