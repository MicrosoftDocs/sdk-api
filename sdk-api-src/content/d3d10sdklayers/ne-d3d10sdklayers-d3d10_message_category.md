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

# D3D10_MESSAGE_CATEGORY enumeration


## -description


Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="https://msdn.microsoft.com/c7ed2819-d726-4719-b46c-03c001b9b40d">ID3D10InfoQueue::GetMessage</a> and when adding a message with <a href="https://msdn.microsoft.com/d31a0c87-b895-49e2-96e6-1df68db3995b">ID3D10InfoQueue::AddMessage</a>. When creating an <a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.


## -enum-fields




### -field D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED

User defined message. See <a href="https://msdn.microsoft.com/d31a0c87-b895-49e2-96e6-1df68db3995b">ID3D10InfoQueue::AddMessage</a>.


### -field D3D10_MESSAGE_CATEGORY_MISCELLANEOUS


### -field D3D10_MESSAGE_CATEGORY_INITIALIZATION


### -field D3D10_MESSAGE_CATEGORY_CLEANUP


### -field D3D10_MESSAGE_CATEGORY_COMPILATION


### -field D3D10_MESSAGE_CATEGORY_STATE_CREATION


### -field D3D10_MESSAGE_CATEGORY_STATE_SETTING


### -field D3D10_MESSAGE_CATEGORY_STATE_GETTING


### -field D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION


### -field D3D10_MESSAGE_CATEGORY_EXECUTION


### -field D3D10_MESSAGE_CATEGORY_SHADER




## -remarks



This is part of the Information Queue feature. See <a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

