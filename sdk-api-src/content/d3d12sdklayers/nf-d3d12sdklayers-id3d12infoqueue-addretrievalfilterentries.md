---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddRetrievalFilterEntries
title: ID3D12InfoQueue::AddRetrievalFilterEntries (d3d12sdklayers.h)
description: Add storage filters to the top of the retrieval-filter stack. (ID3D12InfoQueue.AddRetrievalFilterEntries)
helpviewer_keywords: ["AddRetrievalFilterEntries","AddRetrievalFilterEntries method","AddRetrievalFilterEntries method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","AddRetrievalFilterEntries method","ID3D12InfoQueue.AddRetrievalFilterEntries","ID3D12InfoQueue::AddRetrievalFilterEntries","d3d12sdklayers/ID3D12InfoQueue::AddRetrievalFilterEntries","direct3d12.id3d12infoqueue_addretrievalfilterentries"]
old-location: direct3d12\id3d12infoqueue_addretrievalfilterentries.htm
tech.root: direct3d12
ms.assetid: 66430A0A-0279-4D2D-A34D-D49C7940DB87
ms.date: 12/05/2018
ms.keywords: AddRetrievalFilterEntries, AddRetrievalFilterEntries method, AddRetrievalFilterEntries method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,AddRetrievalFilterEntries method, ID3D12InfoQueue.AddRetrievalFilterEntries, ID3D12InfoQueue::AddRetrievalFilterEntries, d3d12sdklayers/ID3D12InfoQueue::AddRetrievalFilterEntries, direct3d12.id3d12infoqueue_addretrievalfilterentries
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
 - ID3D12InfoQueue::AddRetrievalFilterEntries
 - d3d12sdklayers/ID3D12InfoQueue::AddRetrievalFilterEntries
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
 - ID3D12InfoQueue.AddRetrievalFilterEntries
---

# ID3D12InfoQueue::AddRetrievalFilterEntries


## -description

Add storage filters to the top of the retrieval-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>*</b>

Array of retrieval filters.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

The following code example shows how to use this method:




``` syntax
 
D3D12_MESSAGE_CATEGORY cats[] = { ..., ..., ... };
D3D12_MESSAGE_SEVERITY sevs[] = { ..., ..., ... };
D3D12_MESSAGE_ID ids[] = { ..., ..., ... };

D3D12_INFO_QUEUE_FILTER filter;
memset( &filter, 0, sizeof(filter) );

// To set the type of messages to allow, 
// set filter.AllowList as follows:
filter.AllowList.NumCategories = _countof(cats);
filter.AllowList.pCategoryList = cats;
filter.AllowList.NumSeverities = _countof(sevs);
filter.AllowList.pSeverityList = sevs;
filter.AllowList.NumIDs = _countof(ids);
filter.AllowList.pIDList = ids;

// To set the type of messages to deny, set filter.DenyList 
// similarly to the preceding filter.AllowList.

// The following single call sets all of the preceding information.
hr = infoQueue->AddRetrievalFilterEntries( &filter );
 

```


## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
