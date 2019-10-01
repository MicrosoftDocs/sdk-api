---
UID: NF:dxgidebug.IDXGIInfoQueue.AddStorageFilterEntries
title: IDXGIInfoQueue::AddStorageFilterEntries (dxgidebug.h)
author: windows-sdk-content
description: Adds storage filters to the top of the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_addstoragefilterentries.htm
tech.root: direct3ddxgi
ms.assetid: 34FC5AE3-7B72-4480-ACFA-53C7FB5425DA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddStorageFilterEntries, AddStorageFilterEntries method [DXGI], AddStorageFilterEntries method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddStorageFilterEntries method, IDXGIInfoQueue.AddStorageFilterEntries, IDXGIInfoQueue::AddStorageFilterEntries, direct3ddxgi.idxgiinfoqueue_addstoragefilterentries, dxgidebug/IDXGIInfoQueue::AddStorageFilterEntries
ms.topic: method
f1_keywords: 
 - "dxgidebug/IDXGIInfoQueue.AddStorageFilterEntries"
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
 - IDXGIInfoQueue.AddStorageFilterEntries
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIInfoQueue::AddStorageFilterEntries


## -description


Adds storage filters to the top of the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that produced the filters.


### -param pFilter [in]

An array of <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter">DXGI_INFO_QUEUE_FILTER</a> structures that describe the filters.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
 

 

