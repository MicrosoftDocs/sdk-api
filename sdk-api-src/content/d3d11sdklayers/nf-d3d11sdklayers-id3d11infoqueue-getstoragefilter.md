---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetStorageFilter
title: ID3D11InfoQueue::GetStorageFilter
author: windows-sdk-content
description: Get the storage filter at the top of the storage-filter stack.
old-location: direct3d11\id3d11infoqueue_getstoragefilter.htm
old-project: direct3d11
ms.assetid: 87c9d6f0-8a3d-47d4-bfcb-369ec9cbf01a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 825c16d1-ee7b-8b61-1f92-96e2717bbbee, GetStorageFilter, GetStorageFilter method [Direct3D 11], GetStorageFilter method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetStorageFilter method, ID3D11InfoQueue.GetStorageFilter, ID3D11InfoQueue::GetStorageFilter, d3d11sdklayers/ID3D11InfoQueue::GetStorageFilter, direct3d11.id3d11infoqueue_getstoragefilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11sdklayers.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.GetStorageFilter
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::GetStorageFilter


## -description


Get the storage filter at the top of the storage-filter stack.


## -parameters




### -param pFilter [out, optional]

Type: <b><a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">D3D11_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.


### -param pFilterByteLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>

Size of the storage filter in bytes. If pFilter is <b>NULL</b>, the size of the storage filter will be output to this parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

