---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters
title: IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters
author: windows-sdk-content
description: Gets the number of messages that can pass through a retrieval filter.
old-location: direct3ddxgi\idxgiinfoqueue_getnumstoredmessagesallowedbyretrievalfilters.htm
tech.root: direct3ddxgi
ms.assetid: 1BFFEE9F-7902-41B7-9607-BD0E955FBD8B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNumStoredMessagesAllowedByRetrievalFilters, GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI], GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumStoredMessagesAllowedByRetrievalFilters method, IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters, IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters, direct3ddxgi.idxgiinfoqueue_getnumstoredmessagesallowedbyretrievalfilters, dxgidebug/IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters
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
 - IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters


## -description


Gets the number of messages that can pass through a retrieval filter.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.


## -returns



Returns the number of messages that can pass through a retrieval filter.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

