---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumStoredMessages
title: IDXGIInfoQueue::GetNumStoredMessages
author: windows-sdk-content
description: Gets the number of messages currently stored in the message queue.
old-location: direct3ddxgi\idxgiinfoqueue_getnumstoredmessages.htm
old-project: direct3ddxgi
ms.assetid: 81556BB3-D8B8-4868-8B21-C9E01C3F183E
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetNumStoredMessages, GetNumStoredMessages method [DXGI], GetNumStoredMessages method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumStoredMessages method, IDXGIInfoQueue.GetNumStoredMessages, IDXGIInfoQueue::GetNumStoredMessages, direct3ddxgi.idxgiinfoqueue_getnumstoredmessages, dxgidebug/IDXGIInfoQueue::GetNumStoredMessages
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
 - IDXGIInfoQueue.GetNumStoredMessages
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::GetNumStoredMessages


## -description


Gets the number of messages currently stored in the message queue.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.


## -returns



Returns the number of messages currently stored in the message queue.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

