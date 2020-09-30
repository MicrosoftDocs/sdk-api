---
UID: NF:bdaiface.IEnumPIDMap.Skip
title: IEnumPIDMap::Skip (bdaiface.h)
description: The Skip method skips the specified number of elements in the collection.
helpviewer_keywords: ["IEnumPIDMap interface [DirectShow]","Skip method","IEnumPIDMap.Skip","IEnumPIDMap::Skip","IEnumPIDMapSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumPIDMap interface","bdaiface/IEnumPIDMap::Skip","dshow.ienumpidmap_skip"]
old-location: dshow\ienumpidmap_skip.htm
tech.root: dshow
ms.assetid: e611e5a0-beb1-4a31-974a-29b2b8349a17
ms.date: 12/05/2018
ms.keywords: IEnumPIDMap interface [DirectShow],Skip method, IEnumPIDMap.Skip, IEnumPIDMap::Skip, IEnumPIDMapSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumPIDMap interface, bdaiface/IEnumPIDMap::Skip, dshow.ienumpidmap_skip
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
 - IEnumPIDMap::Skip
 - bdaiface/IEnumPIDMap::Skip
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
 - IEnumPIDMap.Skip
---

# IEnumPIDMap::Skip


## -description

The <code>Skip</code> method skips the specified number of elements in the collection.

## -parameters

### -param cRecords [in]

Specifies the number of elements to skip.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the collection.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap Interface</a>