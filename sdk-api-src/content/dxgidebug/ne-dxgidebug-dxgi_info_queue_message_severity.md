---
UID: NE:dxgidebug.DXGI_INFO_QUEUE_MESSAGE_SEVERITY
title: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
author: windows-sdk-content
description: Values that specify debug message severity levels for an information queue.
old-location: direct3ddxgi\dxgi_info_queue_message_severity.htm
tech.root: direct3ddxgi
ms.assetid: 99F9DDC8-5CCF-4991-94AD-0A399932F5B3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXGI_INFO_QUEUE_MESSAGE_SEVERITY, DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration [DXGI], DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING, direct3ddxgi.dxgi_info_queue_message_severity, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_INFO_QUEUE_MESSAGE_SEVERITY
product: Windows
targetos: Windows
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
req.redist: 
---

# DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration


## -description


Values that specify debug message severity levels for an information queue.


## -enum-fields




### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION

Defines some type of corruption that has occurred.


### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR

Defines an error message.


### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING

Defines a warning message.


### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO

Defines an information message.


### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE

Defines a message other than corruption, error, warning, or information.


## -remarks



Use this enumeration when you call <a href="https://msdn.microsoft.com/208C3253-09AE-4379-808D-BA0BECC59BF8">IDXGIInfoQueue::GetMessage</a> to retrieve a message and when you call <a href="https://msdn.microsoft.com/965DA310-D082-4970-BCD1-F15F44C074D0">IDXGIInfoQueue::AddMessage</a> to add a message. Also, use this enumeration with <a href="https://msdn.microsoft.com/30245BF0-C0AF-4780-A55F-D55A331427FA">IDXGIInfoQueue::AddApplicationMessage</a>.



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

