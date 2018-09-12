---
UID: NF:dxgidebug.IDXGIInfoQueue.GetStorageFilter
title: IDXGIInfoQueue::GetStorageFilter
author: windows-sdk-content
description: Gets the storage filter at the top of the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_getstoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: C0709ECD-94CC-4745-A811-4180EC763CFC
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetStorageFilter, GetStorageFilter method [DXGI], GetStorageFilter method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetStorageFilter method, IDXGIInfoQueue.GetStorageFilter, IDXGIInfoQueue::GetStorageFilter, direct3ddxgi.idxgiinfoqueue_getstoragefilter, dxgidebug/IDXGIInfoQueue::GetStorageFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDXGIInfoQueue.GetStorageFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::GetStorageFilter


## -description


Gets the storage filter at the top of the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the filter.


### -param pFilter [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/95E68ECE-39D2-4D16-9A8F-FE6E527A83E3">DXGI_INFO_QUEUE_FILTER</a> structure that describes the filter.


### -param pFilterByteLength [in, out]

A pointer to a variable that receives the size, in bytes, of the filter description to which <i>pFilter</i> points. If <i>pFilter</i> is <b>NULL</b>, <b>GetStorageFilter</b> outputs the size of the storage filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

