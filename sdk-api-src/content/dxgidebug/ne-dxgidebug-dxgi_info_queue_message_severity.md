---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

