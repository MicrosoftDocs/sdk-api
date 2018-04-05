---
UID: NF:dxgidebug.IDXGIInfoQueue.GetMessageCountLimit
title: IDXGIInfoQueue::GetMessageCountLimit method
author: windows-driver-content
description: Gets the maximum number of messages that can be added to the message queue.
old-location: direct3ddxgi\idxgiinfoqueue_getmessagecountlimit.htm
old-project: direct3ddxgi
ms.assetid: F9700374-255D-423E-8E60-4FE7FFA9E807
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetMessageCountLimit method [DXGI], GetMessageCountLimit method [DXGI], IDXGIInfoQueue interface, GetMessageCountLimit,IDXGIInfoQueue.GetMessageCountLimit, IDXGIInfoQueue, IDXGIInfoQueue interface [DXGI], GetMessageCountLimit method, IDXGIInfoQueue::GetMessageCountLimit, direct3ddxgi.idxgiinfoqueue_getmessagecountlimit, dxgidebug/IDXGIInfoQueue::GetMessageCountLimit
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
-	IDXGIInfoQueue.GetMessageCountLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::GetMessageCountLimit method


## -description


Gets the maximum number of messages that can be added to the message queue.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.


## -returns



Returns the maximum number of messages that can be added to the queue. –1 means no limit.




## -remarks



When the number of messages in the message queue reaches the maximum limit, new messages coming in push old messages out.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

