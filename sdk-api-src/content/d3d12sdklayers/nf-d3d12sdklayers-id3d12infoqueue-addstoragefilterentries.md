---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddStorageFilterEntries
title: ID3D12InfoQueue::AddStorageFilterEntries method
author: windows-driver-content
description: Add storage filters to the top of the storage-filter stack.
old-location: direct3d12\id3d12infoqueue_addstoragefilterentries.htm
old-project: direct3d12
ms.assetid: 24AEAE62-D2D8-4A0C-9EB3-6D3942BC86D9
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: AddStorageFilterEntries method, AddStorageFilterEntries method, ID3D12InfoQueue interface, AddStorageFilterEntries,ID3D12InfoQueue.AddStorageFilterEntries, ID3D12InfoQueue, ID3D12InfoQueue interface, AddStorageFilterEntries method, ID3D12InfoQueue::AddStorageFilterEntries, d3d12sdklayers/ID3D12InfoQueue::AddStorageFilterEntries, direct3d12.id3d12infoqueue_addstoragefilterentries
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12sdklayers.h
api_name:
-	ID3D12InfoQueue.AddStorageFilterEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12InfoQueue::AddStorageFilterEntries method


## -description



          Add storage filters to the top of the storage-filter stack.


        


## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/5CD64E71-8530-43FB-B441-25C61ED6F317">D3D12_INFO_QUEUE_FILTER</a>*</b>


            Array of storage filters.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

