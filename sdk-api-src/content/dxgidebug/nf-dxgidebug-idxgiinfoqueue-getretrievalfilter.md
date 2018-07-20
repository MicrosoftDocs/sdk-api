---
UID: NF:dxgidebug.IDXGIInfoQueue.GetRetrievalFilter
title: IDXGIInfoQueue::GetRetrievalFilter
author: windows-sdk-content
description: Gets the retrieval filter at the top of the retrieval-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_getretrievalfilter.htm
old-project: direct3ddxgi
ms.assetid: 95907EF0-858B-4CDF-A112-6E59138769BD
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetRetrievalFilter, GetRetrievalFilter method [DXGI], GetRetrievalFilter method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetRetrievalFilter method, IDXGIInfoQueue.GetRetrievalFilter, IDXGIInfoQueue::GetRetrievalFilter, direct3ddxgi.idxgiinfoqueue_getretrievalfilter, dxgidebug/IDXGIInfoQueue::GetRetrievalFilter
ms.prod: windows
ms.technology: windows-sdk
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
 - IDXGIInfoQueue.GetRetrievalFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::GetRetrievalFilter


## -description


Gets the retrieval filter at the top of the retrieval-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the filter.


### -param pFilter [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/95E68ECE-39D2-4D16-9A8F-FE6E527A83E3">DXGI_INFO_QUEUE_FILTER</a> structure that describes the filter.


### -param pFilterByteLength [in, out]

A pointer to a variable that receives the size, in bytes, of the filter description to which <i>pFilter</i> points. If <i>pFilter</i> is <b>NULL</b>, <b>GetRetrievalFilter</b> outputs the size of the retrieval filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

