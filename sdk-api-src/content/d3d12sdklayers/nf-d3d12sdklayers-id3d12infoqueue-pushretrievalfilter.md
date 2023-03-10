---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.PushRetrievalFilter
title: ID3D12InfoQueue::PushRetrievalFilter (d3d12sdklayers.h)
description: Push a retrieval filter onto the retrieval-filter stack. (ID3D12InfoQueue.PushRetrievalFilter)
helpviewer_keywords: ["ID3D12InfoQueue interface","PushRetrievalFilter method","ID3D12InfoQueue.PushRetrievalFilter","ID3D12InfoQueue::PushRetrievalFilter","PushRetrievalFilter","PushRetrievalFilter method","PushRetrievalFilter method","ID3D12InfoQueue interface","d3d12sdklayers/ID3D12InfoQueue::PushRetrievalFilter","direct3d12.id3d12infoqueue_pushretrievalfilter"]
old-location: direct3d12\id3d12infoqueue_pushretrievalfilter.htm
tech.root: direct3d12
ms.assetid: 4270B455-7112-4BCD-B8B9-D60B7FEADD9E
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue interface,PushRetrievalFilter method, ID3D12InfoQueue.PushRetrievalFilter, ID3D12InfoQueue::PushRetrievalFilter, PushRetrievalFilter, PushRetrievalFilter method, PushRetrievalFilter method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::PushRetrievalFilter, direct3d12.id3d12infoqueue_pushretrievalfilter
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
 - ID3D12InfoQueue::PushRetrievalFilter
 - d3d12sdklayers/ID3D12InfoQueue::PushRetrievalFilter
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
 - ID3D12InfoQueue.PushRetrievalFilter
---

# ID3D12InfoQueue::PushRetrievalFilter


## -description

Push a retrieval filter onto the retrieval-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>*</b>

Pointer to a retrieval filter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
