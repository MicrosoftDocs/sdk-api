---
UID: NF:dxgidebug.IDXGIInfoQueue.AddApplicationMessage
title: IDXGIInfoQueue::AddApplicationMessage
author: windows-sdk-content
description: Adds a user-defined message to the message queue and sends that message to the debug output.
old-location: direct3ddxgi\idxgiinfoqueue_addapplicationmessage.htm
tech.root: direct3ddxgi
ms.assetid: 30245BF0-C0AF-4780-A55F-D55A331427FA
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AddApplicationMessage, AddApplicationMessage method [DXGI], AddApplicationMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddApplicationMessage method, IDXGIInfoQueue.AddApplicationMessage, IDXGIInfoQueue::AddApplicationMessage, direct3ddxgi.idxgiinfoqueue_addapplicationmessage, dxgidebug/IDXGIInfoQueue::AddApplicationMessage
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
 - IDXGIInfoQueue.AddApplicationMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgidebug.h
: 
- IDXGIInfoQueue.AddApplicationMessage
: 
---

# IDXGIInfoQueue::AddApplicationMessage


## -description


Adds a user-defined message to the message queue and sends that message to the debug output.


## -parameters




### -param Severity [in]

A <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.


### -param pDescription [in]

The message string.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

