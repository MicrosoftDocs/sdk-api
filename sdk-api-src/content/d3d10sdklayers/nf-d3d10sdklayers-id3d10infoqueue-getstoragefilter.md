---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetStorageFilter
title: ID3D10InfoQueue::GetStorageFilter
author: windows-driver-content
description: Get the storage filter at the top of the storage-filter stack.
old-location: direct3d10\id3d10infoqueue_getstoragefilter.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getstoragefilter.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10InfoQueue.GetStorageFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::GetStorageFilter


## -description


Get the storage filter at the top of the storage-filter stack.


## -parameters




### -param pFilter [out]

Type: <b><a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.


### -param pFilterByteLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>

Size of the storage filter in bytes. If pFilter is <b>NULL</b>, the size of the storage filter will be output to this parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

