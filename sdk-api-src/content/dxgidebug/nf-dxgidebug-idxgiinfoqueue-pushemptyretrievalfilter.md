---
UID: NF:dxgidebug.IDXGIInfoQueue.PushEmptyRetrievalFilter
title: IDXGIInfoQueue::PushEmptyRetrievalFilter
author: windows-sdk-content
description: Pushes an empty retrieval filter onto the retrieval-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushemptyretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: F6125FB9-EA1B-4052-A527-F4E5FAEE5C61
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushEmptyRetrievalFilter method, IDXGIInfoQueue.PushEmptyRetrievalFilter, IDXGIInfoQueue::PushEmptyRetrievalFilter, PushEmptyRetrievalFilter, PushEmptyRetrievalFilter method [DXGI], PushEmptyRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushemptyretrievalfilter, dxgidebug/IDXGIInfoQueue::PushEmptyRetrievalFilter
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
 - IDXGIInfoQueue.PushEmptyRetrievalFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::PushEmptyRetrievalFilter


## -description


Pushes an empty retrieval filter onto the retrieval-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the empty retrieval filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



An empty retrieval filter allows all messages to pass through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

