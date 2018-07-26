---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddStorageFilterEntries
title: ID3D10InfoQueue::AddStorageFilterEntries
author: windows-sdk-content
description: Add storage filters to the top of the storage-filter stack.
old-location: direct3d10\id3d10infoqueue_addstoragefilterentries.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addstoragefilterentries.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 4fab9df2-2a5e-b48c-409f-cf4ef5f8bf7c, AddStorageFilterEntries, AddStorageFilterEntries method [Direct3D 10], AddStorageFilterEntries method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddStorageFilterEntries method, ID3D10InfoQueue.AddStorageFilterEntries, ID3D10InfoQueue::AddStorageFilterEntries, d3d10sdklayers/ID3D10InfoQueue::AddStorageFilterEntries, direct3d10.id3d10infoqueue_addstoragefilterentries
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_MESSAGE_SEVERITY
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
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::AddStorageFilterEntries


## -description


Add storage filters to the top of the storage-filter stack.


## -parameters




### -param pFilter [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb205313(v=VS.85).aspx">D3D10_INFO_QUEUE_FILTER</a>*</b>

Array of storage filters (see <a href="https://msdn.microsoft.com/library/Bb205313(v=VS.85).aspx">D3D10_INFO_QUEUE_FILTER</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A storage filter defines a grouping of debug messages that should be allowed into the info queue.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

