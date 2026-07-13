---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddRetrievalFilterEntries
title: ID3D10InfoQueue::AddRetrievalFilterEntries (d3d10sdklayers.h)
description: Add storage filters to the top of the retrieval-filter stack. (ID3D10InfoQueue.AddRetrievalFilterEntries)
helpviewer_keywords: ["5ea15176-4f13-65d2-afa6-3051b0d0908a","AddRetrievalFilterEntries","AddRetrievalFilterEntries method [Direct3D 10]","AddRetrievalFilterEntries method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","AddRetrievalFilterEntries method","ID3D10InfoQueue.AddRetrievalFilterEntries","ID3D10InfoQueue::AddRetrievalFilterEntries","d3d10sdklayers/ID3D10InfoQueue::AddRetrievalFilterEntries","direct3d10.id3d10infoqueue_addretrievalfilterentries"]
old-location: direct3d10\id3d10infoqueue_addretrievalfilterentries.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addretrievalfilterentries.htm
ms.date: 12/05/2018
ms.keywords: 5ea15176-4f13-65d2-afa6-3051b0d0908a, AddRetrievalFilterEntries, AddRetrievalFilterEntries method [Direct3D 10], AddRetrievalFilterEntries method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddRetrievalFilterEntries method, ID3D10InfoQueue.AddRetrievalFilterEntries, ID3D10InfoQueue::AddRetrievalFilterEntries, d3d10sdklayers/ID3D10InfoQueue::AddRetrievalFilterEntries, direct3d10.id3d10infoqueue_addretrievalfilterentries
req.header: d3d10sdklayers.h
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
 - ID3D10InfoQueue::AddRetrievalFilterEntries
 - d3d10sdklayers/ID3D10InfoQueue::AddRetrievalFilterEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.AddRetrievalFilterEntries
---

# ID3D10InfoQueue::AddRetrievalFilterEntries


## -description

Add storage filters to the top of the retrieval-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>*</b>

Array of retrieval filters (see <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A retrieval filter is used to define a subgroup of the messages that are already in the info queue.  
      Retrieval filters affect the messages that will be returned by <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage">ID3D10InfoQueue::GetMessage</a>.

The number of messages already in the info queue that will be allowed through the retrieval filter can be determined 
      by calling <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-getnumstoredmessagesallowedbyretrievalfilter">ID3D10InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
