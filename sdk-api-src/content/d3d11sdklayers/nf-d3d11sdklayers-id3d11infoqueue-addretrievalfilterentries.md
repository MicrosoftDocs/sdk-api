---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddRetrievalFilterEntries
title: ID3D11InfoQueue::AddRetrievalFilterEntries (d3d11sdklayers.h)
description: Add storage filters to the top of the retrieval-filter stack. (ID3D11InfoQueue.AddRetrievalFilterEntries)
helpviewer_keywords: ["9da78ed8-cfc3-47cd-e2a8-318199bba80d","AddRetrievalFilterEntries","AddRetrievalFilterEntries method [Direct3D 11]","AddRetrievalFilterEntries method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","AddRetrievalFilterEntries method","ID3D11InfoQueue.AddRetrievalFilterEntries","ID3D11InfoQueue::AddRetrievalFilterEntries","d3d11sdklayers/ID3D11InfoQueue::AddRetrievalFilterEntries","direct3d11.id3d11infoqueue_addretrievalfilterentries"]
old-location: direct3d11\id3d11infoqueue_addretrievalfilterentries.htm
tech.root: direct3d11
ms.assetid: 638d6af7-d425-4865-8124-dd7cd0dc6927
ms.date: 12/05/2018
ms.keywords: 9da78ed8-cfc3-47cd-e2a8-318199bba80d, AddRetrievalFilterEntries, AddRetrievalFilterEntries method [Direct3D 11], AddRetrievalFilterEntries method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddRetrievalFilterEntries method, ID3D11InfoQueue.AddRetrievalFilterEntries, ID3D11InfoQueue::AddRetrievalFilterEntries, d3d11sdklayers/ID3D11InfoQueue::AddRetrievalFilterEntries, direct3d11.id3d11infoqueue_addretrievalfilterentries
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue::AddRetrievalFilterEntries
 - d3d11sdklayers/ID3D11InfoQueue::AddRetrievalFilterEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.AddRetrievalFilterEntries
---

# ID3D11InfoQueue::AddRetrievalFilterEntries


## -description

Add storage filters to the top of the retrieval-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>*</b>

Array of retrieval filters (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The following code example shows how to use <b>ID3D11InfoQueue::AddRetrievalFilterEntries</b>:


```

D3D11_MESSAGE_CATEGORY cats[] = { ..., ..., ... };
D3D11_MESSAGE_SEVERITY sevs[] = { ..., ..., ... };
UINT ids[] = { ..., ..., ... };

D3D11_INFO_QUEUE_FILTER filter;
memset( &filter, 0, sizeof(filter) );

// To set the type of messages to allow, 
// set filter.AllowList as follows:
filter.AllowList.NumCategories = sizeof(cats / sizeof(D3D11_MESSAGE_CATEGORY)); 
filter.AllowList.pCategoryList = cats;
filter.AllowList.NumSeverities = sizeof(sevs / sizeof(D3D11_MESSAGE_SEVERITY)); 
filter.AllowList.pSeverityList = sevs;
filter.AllowList.NumIDs = sizeof(ids) / sizeof(UINT);
filter.AllowList.pIDList = ids;

// To set the type of messages to deny, set filter.DenyList 
// similarly to the preceding filter.AllowList.

// The following single call sets all of the preceding information.
hr = infoQueue->AddRetrievalFilterEntries( &filter );

```

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
