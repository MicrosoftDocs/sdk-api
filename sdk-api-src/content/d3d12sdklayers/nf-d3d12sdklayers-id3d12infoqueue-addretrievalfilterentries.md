---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddRetrievalFilterEntries
title: ID3D12InfoQueue::AddRetrievalFilterEntries
author: windows-sdk-content
description: Add storage filters to the top of the retrieval-filter stack.
old-location: direct3d12\id3d12infoqueue_addretrievalfilterentries.htm
old-project: direct3d12
ms.assetid: 66430A0A-0279-4D2D-A34D-D49C7940DB87
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: AddRetrievalFilterEntries, AddRetrievalFilterEntries method, AddRetrievalFilterEntries method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,AddRetrievalFilterEntries method, ID3D12InfoQueue.AddRetrievalFilterEntries, ID3D12InfoQueue::AddRetrievalFilterEntries, d3d12sdklayers/ID3D12InfoQueue::AddRetrievalFilterEntries, direct3d12.id3d12infoqueue_addretrievalfilterentries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.AddRetrievalFilterEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12InfoQueue::AddRetrievalFilterEntries


## -description



          Add storage filters to the top of the retrieval-filter stack.




## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/5CD64E71-8530-43FB-B441-25C61ED6F317">D3D12_INFO_QUEUE_FILTER</a>*</b>

Array of retrieval filters.




## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -remarks



The following code example shows how to use this method:



<pre class="syntax" xml:space="preserve"><code> 
D3D12_MESSAGE_CATEGORY cats[] = { ..., ..., ... };
D3D12_MESSAGE_SEVERITY sevs[] = { ..., ..., ... };
UINT ids[] = { ..., ..., ... };

D3D12_INFO_QUEUE_FILTER filter;
memset( &amp;filter, 0, sizeof(filter) );

// To set the type of messages to allow, 
// set filter.AllowList as follows:
filter.AllowList.NumCategories = sizeof(cats / sizeof(D3D12_MESSAGE_CATEGORY)); 
filter.AllowList.pCategoryList = cats;
filter.AllowList.NumSeverities = sizeof(sevs / sizeof(D3D12_MESSAGE_SEVERITY)); 
filter.AllowList.pSeverityList = sevs;
filter.AllowList.NumIDs = sizeof(ids) / sizeof(UINT);
filter.AllowList.pIDList = ids;

// To set the type of messages to deny, set filter.DenyList 
// similarly to the preceding filter.AllowList.

// The following single call sets all of the preceding information.
hr = infoQueue-&gt;AddRetrievalFilterEntries( &amp;filter );
 
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

