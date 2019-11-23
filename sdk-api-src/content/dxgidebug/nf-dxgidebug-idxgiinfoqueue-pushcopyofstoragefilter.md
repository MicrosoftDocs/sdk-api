---
UID: NF:dxgidebug.IDXGIInfoQueue.PushCopyOfStorageFilter
title: IDXGIInfoQueue::PushCopyOfStorageFilter (dxgidebug.h)

description: Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushcopyofstoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: 1CD32898-90B1-4523-8C97-985CA9F7D92B

ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushCopyOfStorageFilter method, IDXGIInfoQueue.PushCopyOfStorageFilter, IDXGIInfoQueue::PushCopyOfStorageFilter, PushCopyOfStorageFilter, PushCopyOfStorageFilter method [DXGI], PushCopyOfStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushcopyofstoragefilter, dxgidebug/IDXGIInfoQueue::PushCopyOfStorageFilter
ms.topic: method
f1_keywords: 
 - "dxgidebug/IDXGIInfoQueue.PushCopyOfStorageFilter"
dev_langs:
 - c++
req.header: dxgidebug.h
req.include-header: 
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
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.PushCopyOfStorageFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIInfoQueue::PushCopyOfStorageFilter


## -description


Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the copy of the storage filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
 

 

