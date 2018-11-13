---
UID: NF:dxgidebug.IDXGIInfoQueue.PushDenyAllStorageFilter
title: IDXGIInfoQueue::PushDenyAllStorageFilter
author: windows-sdk-content
description: Pushes a deny-all storage filter onto the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushdenyallstoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: 7985F43F-B0D3-4FF1-83D9-EEB568B29664
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushDenyAllStorageFilter method, IDXGIInfoQueue.PushDenyAllStorageFilter, IDXGIInfoQueue::PushDenyAllStorageFilter, PushDenyAllStorageFilter, PushDenyAllStorageFilter method [DXGI], PushDenyAllStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushdenyallstoragefilter, dxgidebug/IDXGIInfoQueue::PushDenyAllStorageFilter
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
 - IDXGIInfoQueue.PushDenyAllStorageFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::PushDenyAllStorageFilter


## -description


Pushes a deny-all storage filter onto the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



A deny-all storage filter prevents all messages from passing through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

