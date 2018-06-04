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

# D3D11_MESSAGE_CATEGORY enumeration


## -description


Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="https://msdn.microsoft.com/685cddc5-cedd-410f-a693-665d2d69402e">ID3D11InfoQueue::GetMessage</a> and when adding a message with <a href="https://msdn.microsoft.com/7265a273-327a-482b-9d47-6931e031cff8">ID3D11InfoQueue::AddMessage</a>. When creating an <a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.


## -enum-fields




### -field D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED

User defined message. See <a href="https://msdn.microsoft.com/7265a273-327a-482b-9d47-6931e031cff8">ID3D11InfoQueue::AddMessage</a>.


### -field D3D11_MESSAGE_CATEGORY_MISCELLANEOUS


### -field D3D11_MESSAGE_CATEGORY_INITIALIZATION


### -field D3D11_MESSAGE_CATEGORY_CLEANUP


### -field D3D11_MESSAGE_CATEGORY_COMPILATION


### -field D3D11_MESSAGE_CATEGORY_STATE_CREATION


### -field D3D11_MESSAGE_CATEGORY_STATE_SETTING


### -field D3D11_MESSAGE_CATEGORY_STATE_GETTING


### -field D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION


### -field D3D11_MESSAGE_CATEGORY_EXECUTION


### -field D3D11_MESSAGE_CATEGORY_SHADER

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -remarks



This is part of the Information Queue feature. See <a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Layer Enumerations</a>
 

 

