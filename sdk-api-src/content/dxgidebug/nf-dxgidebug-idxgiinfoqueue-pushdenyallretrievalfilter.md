---
UID: NF:dxgidebug.IDXGIInfoQueue.PushDenyAllRetrievalFilter
title: IDXGIInfoQueue::PushDenyAllRetrievalFilter
author: windows-sdk-content
description: Pushes a deny-all retrieval filter onto the retrieval-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushdenyallretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: 104C5BAD-D1FF-47EC-A1FA-C4B32EA4DFB6
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushDenyAllRetrievalFilter method, IDXGIInfoQueue.PushDenyAllRetrievalFilter, IDXGIInfoQueue::PushDenyAllRetrievalFilter, PushDenyAllRetrievalFilter, PushDenyAllRetrievalFilter method [DXGI], PushDenyAllRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushdenyallretrievalfilter, dxgidebug/IDXGIInfoQueue::PushDenyAllRetrievalFilter
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
 - IDXGIInfoQueue.PushDenyAllRetrievalFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::PushDenyAllRetrievalFilter


## -description


Pushes a deny-all retrieval filter onto the retrieval-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the deny-all retrieval filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



A deny-all retrieval filter prevents all messages from passing through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

