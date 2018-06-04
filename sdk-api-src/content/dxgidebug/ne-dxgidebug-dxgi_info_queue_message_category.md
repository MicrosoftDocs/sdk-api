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

# DXGI_INFO_QUEUE_MESSAGE_CATEGORY enumeration


## -description


Values that specify categories of debug messages.


## -enum-fields




### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_UNKNOWN

Unknown category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_MISCELLANEOUS

Miscellaneous category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_INITIALIZATION

Initialization category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_CLEANUP

Cleanup category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_COMPILATION

Compilation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_CREATION

State creation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_SETTING

State setting category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_GETTING

State getting category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_RESOURCE_MANIPULATION

Resource manipulation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_EXECUTION

Execution category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_SHADER

Shader category.


## -remarks



Use this enumeration when you call <a href="https://msdn.microsoft.com/208C3253-09AE-4379-808D-BA0BECC59BF8">IDXGIInfoQueue::GetMessage</a> to retrieve a message and when you call <a href="https://msdn.microsoft.com/965DA310-D082-4970-BCD1-F15F44C074D0">IDXGIInfoQueue::AddMessage</a> to add a message. When you create an info queue filter, you can use these values to allow or deny any categories of messages to pass through the storage and retrieval filters.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

