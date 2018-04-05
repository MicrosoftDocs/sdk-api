---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.PushStorageFilter
title: ID3D11InfoQueue::PushStorageFilter method
author: windows-driver-content
description: Push a storage filter onto the storage-filter stack.
old-location: direct3d11\id3d11infoqueue_pushstoragefilter.htm
old-project: direct3d11
ms.assetid: de3f22b0-0642-4aa8-8bb0-008c1e44d3cb
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 8aa4344e-4688-6e7c-8033-8b589f37ce3d, ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], PushStorageFilter method, ID3D11InfoQueue::PushStorageFilter, PushStorageFilter method [Direct3D 11], PushStorageFilter method [Direct3D 11], ID3D11InfoQueue interface, PushStorageFilter,ID3D11InfoQueue.PushStorageFilter, d3d11sdklayers/ID3D11InfoQueue::PushStorageFilter, direct3d11.id3d11infoqueue_pushstoragefilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11InfoQueue.PushStorageFilter
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::PushStorageFilter method


## -description


Push a storage filter onto the storage-filter stack.


## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">D3D11_INFO_QUEUE_FILTER</a>*</b>

Pointer to a storage filter (see <a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">D3D11_INFO_QUEUE_FILTER</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

