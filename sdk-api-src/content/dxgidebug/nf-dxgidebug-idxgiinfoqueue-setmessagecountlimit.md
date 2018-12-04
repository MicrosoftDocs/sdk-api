---
UID: NF:dxgidebug.IDXGIInfoQueue.SetMessageCountLimit
title: IDXGIInfoQueue::SetMessageCountLimit
author: windows-sdk-content
description: Sets the maximum number of messages that can be added to the message queue.
old-location: direct3ddxgi\idxgiinfoqueue_setmessagecountlimit.htm
tech.root: direct3ddxgi
ms.assetid: 77FFF3EA-DEBC-4D92-9C10-E382CD663D20
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetMessageCountLimit method, IDXGIInfoQueue.SetMessageCountLimit, IDXGIInfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [DXGI], SetMessageCountLimit method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setmessagecountlimit, dxgidebug/IDXGIInfoQueue::SetMessageCountLimit
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
 - IDXGIInfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::SetMessageCountLimit


## -description


Sets the maximum number of messages that can be added to the message queue.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that sets the limit on the number of messages.


### -param MessageCountLimit [in]

The maximum number of messages that can be added to the queue. –1 means no limit.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

