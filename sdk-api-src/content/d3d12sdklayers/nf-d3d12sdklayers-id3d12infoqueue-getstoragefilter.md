---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetStorageFilter
title: ID3D12InfoQueue::GetStorageFilter
author: windows-sdk-content
description: Get the storage filter at the top of the storage-filter stack.
old-location: direct3d12\id3d12infoqueue_getstoragefilter.htm
tech.root: direct3d12
ms.assetid: 077C3BA1-9686-4405-A561-4A6A2B128320
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStorageFilter, GetStorageFilter method, GetStorageFilter method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetStorageFilter method, ID3D12InfoQueue.GetStorageFilter, ID3D12InfoQueue::GetStorageFilter, d3d12sdklayers/ID3D12InfoQueue::GetStorageFilter, direct3d12.id3d12infoqueue_getstoragefilter
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.GetStorageFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12InfoQueue::GetStorageFilter


## -description


Get the storage filter at the top of the storage-filter stack.




## -parameters




### -param pFilter [out, optional]

Type: <b><a href="https://msdn.microsoft.com/5CD64E71-8530-43FB-B441-25C61ED6F317">D3D12_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.




### -param pFilterByteLength [in, out]

Type: <b>SIZE_T*</b>

Size of the storage filter in bytes. If <i>pFilter</i> is NULL, the size of the storage filter will be output to this parameter.




## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

