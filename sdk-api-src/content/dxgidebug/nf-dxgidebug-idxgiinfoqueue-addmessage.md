---
UID: NF:dxgidebug.IDXGIInfoQueue.AddMessage
title: IDXGIInfoQueue::AddMessage
author: windows-sdk-content
description: Adds a debug message to the message queue and sends that message to the debug output.
old-location: direct3ddxgi\idxgiinfoqueue_addmessage.htm
old-project: direct3ddxgi
ms.assetid: 965DA310-D082-4970-BCD1-F15F44C074D0
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: AddMessage, AddMessage method [DXGI], AddMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddMessage method, IDXGIInfoQueue.AddMessage, IDXGIInfoQueue::AddMessage, direct3ddxgi.idxgiinfoqueue_addmessage, dxgidebug/IDXGIInfoQueue::AddMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.redist: 
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
 - IDXGIInfoQueue.AddMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::AddMessage


## -description


Adds a debug message to the message queue and sends that message to the debug output.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that produced the message.


### -param Category [in]

A <a href="https://msdn.microsoft.com/B7FA9A43-E234-4C2C-832E-69C827F3BA08">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.


### -param Severity [in]

A <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.


### -param ID [in]

An integer that uniquely identifies the message.


### -param pDescription [in]

The message string.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

