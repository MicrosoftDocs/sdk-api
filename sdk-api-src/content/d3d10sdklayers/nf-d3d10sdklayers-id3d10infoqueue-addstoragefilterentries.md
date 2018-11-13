---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddStorageFilterEntries
title: ID3D10InfoQueue::AddStorageFilterEntries
author: windows-sdk-content
description: Add storage filters to the top of the storage-filter stack.
old-location: direct3d10\id3d10infoqueue_addstoragefilterentries.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addstoragefilterentries.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4fab9df2-2a5e-b48c-409f-cf4ef5f8bf7c, AddStorageFilterEntries, AddStorageFilterEntries method [Direct3D 10], AddStorageFilterEntries method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddStorageFilterEntries method, ID3D10InfoQueue.AddStorageFilterEntries, ID3D10InfoQueue::AddStorageFilterEntries, d3d10sdklayers/ID3D10InfoQueue::AddStorageFilterEntries, direct3d10.id3d10infoqueue_addstoragefilterentries
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
 - ID3D10InfoQueue.AddStorageFilterEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue::AddStorageFilterEntries


## -description


Add storage filters to the top of the storage-filter stack.


## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>*</b>

Array of storage filters (see <a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A storage filter defines a grouping of debug messages that should be allowed into the info queue.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

