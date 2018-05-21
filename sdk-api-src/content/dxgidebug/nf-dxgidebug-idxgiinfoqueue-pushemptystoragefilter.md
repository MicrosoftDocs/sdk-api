---
UID: NF:dxgidebug.IDXGIInfoQueue.PushEmptyStorageFilter
title: IDXGIInfoQueue::PushEmptyStorageFilter
author: windows-driver-content
description: Pushes an empty storage filter onto the storage-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushemptystoragefilter.htm
old-project: direct3ddxgi
ms.assetid: C0DC43B8-4869-49B0-A4D9-6907BCF1CB9E
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushEmptyStorageFilter method, IDXGIInfoQueue.PushEmptyStorageFilter, IDXGIInfoQueue::PushEmptyStorageFilter, PushEmptyStorageFilter, PushEmptyStorageFilter method [DXGI], PushEmptyStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushemptystoragefilter, dxgidebug/IDXGIInfoQueue::PushEmptyStorageFilter
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
-	IDXGIInfoQueue.PushEmptyStorageFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::PushEmptyStorageFilter


## -description


Pushes an empty storage filter onto the storage-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the empty storage filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



An empty storage filter allows all messages to pass through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

