---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddRetrievalFilterEntries
title: ID3D10InfoQueue::AddRetrievalFilterEntries
author: windows-driver-content
description: Add storage filters to the top of the retrieval-filter stack.
old-location: direct3d10\id3d10infoqueue_addretrievalfilterentries.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addretrievalfilterentries.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 5ea15176-4f13-65d2-afa6-3051b0d0908a, AddRetrievalFilterEntries, AddRetrievalFilterEntries method [Direct3D 10], AddRetrievalFilterEntries method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddRetrievalFilterEntries method, ID3D10InfoQueue.AddRetrievalFilterEntries, ID3D10InfoQueue::AddRetrievalFilterEntries, d3d10sdklayers/ID3D10InfoQueue::AddRetrievalFilterEntries, direct3d10.id3d10infoqueue_addretrievalfilterentries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10InfoQueue.AddRetrievalFilterEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::AddRetrievalFilterEntries


## -description


Add storage filters to the top of the retrieval-filter stack.


## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>*</b>

Array of retrieval filters (see <a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A retrieval filter is used to define a subgroup of the messages that are already in the info queue.  
      Retrieval filters affect the messages that will be returned by <a href="https://msdn.microsoft.com/c7ed2819-d726-4719-b46c-03c001b9b40d">ID3D10InfoQueue::GetMessage</a>.

The number of messages already in the info queue that will be allowed through the retrieval filter can be determined 
      by calling <a href="https://msdn.microsoft.com/e7f759b0-d5ee-4777-a16a-315baa09766c">ID3D10InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

