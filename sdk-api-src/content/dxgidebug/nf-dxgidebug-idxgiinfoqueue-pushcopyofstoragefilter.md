---
UID: NF:dxgidebug.IDXGIInfoQueue.PushCopyOfStorageFilter
title: IDXGIInfoQueue::PushCopyOfStorageFilter method
author: windows-driver-content
description: Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushcopyofstoragefilter.htm
old-project: direct3ddxgi
ms.assetid: 1CD32898-90B1-4523-8C97-985CA9F7D92B
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGIInfoQueue, IDXGIInfoQueue interface [DXGI], PushCopyOfStorageFilter method, IDXGIInfoQueue::PushCopyOfStorageFilter, PushCopyOfStorageFilter method [DXGI], PushCopyOfStorageFilter method [DXGI], IDXGIInfoQueue interface, PushCopyOfStorageFilter,IDXGIInfoQueue.PushCopyOfStorageFilter, direct3ddxgi.idxgiinfoqueue_pushcopyofstoragefilter, dxgidebug/IDXGIInfoQueue::PushCopyOfStorageFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGIDebug.dll
api_name:
-	IDXGIInfoQueue.PushCopyOfStorageFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::PushCopyOfStorageFilter method


## -description


Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the copy of the storage filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

