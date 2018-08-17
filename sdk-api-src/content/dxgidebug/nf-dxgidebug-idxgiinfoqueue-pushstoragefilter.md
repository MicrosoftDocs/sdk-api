---
UID: NF:dxgidebug.IDXGIInfoQueue.PushStorageFilter
title: IDXGIInfoQueue::PushStorageFilter
author: windows-sdk-content
description: Pushes a storage filter onto the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushstoragefilter.htm
old-project: direct3ddxgi
ms.assetid: D90738A8-2C9F-4955-9A96-762C650F3B00
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushStorageFilter method, IDXGIInfoQueue.PushStorageFilter, IDXGIInfoQueue::PushStorageFilter, PushStorageFilter, PushStorageFilter method [DXGI], PushStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushstoragefilter, dxgidebug/IDXGIInfoQueue::PushStorageFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.PushStorageFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::PushStorageFilter


## -description


Pushes a storage filter onto the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the filter.


### -param pFilter [in]

A pointer to a <a href="https://msdn.microsoft.com/95E68ECE-39D2-4D16-9A8F-FE6E527A83E3">DXGI_INFO_QUEUE_FILTER</a> structure that describes the filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

