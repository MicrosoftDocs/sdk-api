---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetStorageFilter
title: ID3D12InfoQueue::GetStorageFilter (d3d12sdklayers.h)
author: windows-sdk-content
description: Get the storage filter at the top of the storage-filter stack.
old-location: direct3d12\id3d12infoqueue_getstoragefilter.htm
tech.root: direct3d12
ms.assetid: 077C3BA1-9686-4405-A561-4A6A2B128320
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStorageFilter, GetStorageFilter method, GetStorageFilter method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetStorageFilter method, ID3D12InfoQueue.GetStorageFilter, ID3D12InfoQueue::GetStorageFilter, d3d12sdklayers/ID3D12InfoQueue::GetStorageFilter, direct3d12.id3d12infoqueue_getstoragefilter
ms.topic: method
f1_keywords: 
 - "d3d12sdklayers/ID3D12InfoQueue.GetStorageFilter"
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
ms.custom: 19H1
---

# ID3D12InfoQueue::GetStorageFilter


## -description


Get the storage filter at the top of the storage-filter stack.




## -parameters




### -param pFilter [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.




### -param pFilterByteLength [in, out]

Type: <b>SIZE_T*</b>

Size of the storage filter in bytes. If <i>pFilter</i> is NULL, the size of the storage filter will be output to this parameter.




## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
 

 

