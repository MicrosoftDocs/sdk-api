---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetStorageFilter
title: ID3D10InfoQueue::GetStorageFilter
author: windows-sdk-content
description: Get the storage filter at the top of the storage-filter stack.
old-location: direct3d10\id3d10infoqueue_getstoragefilter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getstoragefilter.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 2a5b558d-3526-acaa-1d02-32a867241cae, GetStorageFilter, GetStorageFilter method [Direct3D 10], GetStorageFilter method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetStorageFilter method, ID3D10InfoQueue.GetStorageFilter, ID3D10InfoQueue::GetStorageFilter, d3d10sdklayers/ID3D10InfoQueue::GetStorageFilter, direct3d10.id3d10infoqueue_getstoragefilter
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetStorageFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue::GetStorageFilter


## -description


Get the storage filter at the top of the storage-filter stack.


## -parameters




### -param pFilter [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205313(v=VS.85).aspx">D3D10_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.


### -param pFilterByteLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>

Size of the storage filter in bytes. If pFilter is <b>NULL</b>, the size of the storage filter will be output to this parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

