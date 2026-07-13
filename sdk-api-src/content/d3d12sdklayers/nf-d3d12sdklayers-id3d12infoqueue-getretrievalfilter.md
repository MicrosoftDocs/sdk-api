---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetRetrievalFilter
title: ID3D12InfoQueue::GetRetrievalFilter (d3d12sdklayers.h)
description: Get the retrieval filter at the top of the retrieval-filter stack. (ID3D12InfoQueue.GetRetrievalFilter)
helpviewer_keywords: ["GetRetrievalFilter","GetRetrievalFilter method","GetRetrievalFilter method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetRetrievalFilter method","ID3D12InfoQueue.GetRetrievalFilter","ID3D12InfoQueue::GetRetrievalFilter","d3d12sdklayers/ID3D12InfoQueue::GetRetrievalFilter","direct3d12.id3d12infoqueue_getretrievalfilter"]
old-location: direct3d12\id3d12infoqueue_getretrievalfilter.htm
tech.root: direct3d12
ms.assetid: A5F4A602-C5C1-402E-9208-D183EEDF6F27
ms.date: 12/05/2018
ms.keywords: GetRetrievalFilter, GetRetrievalFilter method, GetRetrievalFilter method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetRetrievalFilter method, ID3D12InfoQueue.GetRetrievalFilter, ID3D12InfoQueue::GetRetrievalFilter, d3d12sdklayers/ID3D12InfoQueue::GetRetrievalFilter, direct3d12.id3d12infoqueue_getretrievalfilter
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12InfoQueue::GetRetrievalFilter
 - d3d12sdklayers/ID3D12InfoQueue::GetRetrievalFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.GetRetrievalFilter
---

# ID3D12InfoQueue::GetRetrievalFilter


## -description

Get the retrieval filter at the top of the retrieval-filter stack.

## -parameters

### -param pFilter [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>*</b>

Retrieval filter at the top of the retrieval-filter stack.

### -param pFilterByteLength [in, out]

Type: <b>SIZE_T*</b>

Size of the retrieval filter in bytes. If <i>pFilter</i> is NULL, the size of the retrieval filter will be output to this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
