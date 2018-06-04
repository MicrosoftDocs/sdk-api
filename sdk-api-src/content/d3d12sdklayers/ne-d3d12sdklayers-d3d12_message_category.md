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

# D3D12_MESSAGE_CATEGORY enumeration


## -description



          Specifies categories of debug messages. This will identify the category of a message when retrieving a message with <a href="https://msdn.microsoft.com/B7B6D1C4-18FD-492A-8346-CA02FCD3EC4B">ID3D12InfoQueue::GetMessage</a> and when adding a message with <a href="https://msdn.microsoft.com/34AAF9BB-5340-4DB3-87B9-6C26AB6C881C">ID3D12InfoQueue::AddMessage</a>. When creating an info queue filter, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.


        


## -enum-fields




### -field D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED


            Indicates a user defined message, see <a href="https://msdn.microsoft.com/34AAF9BB-5340-4DB3-87B9-6C26AB6C881C">ID3D12InfoQueue::AddMessage</a>.
          


### -field D3D12_MESSAGE_CATEGORY_MISCELLANEOUS


### -field D3D12_MESSAGE_CATEGORY_INITIALIZATION


### -field D3D12_MESSAGE_CATEGORY_CLEANUP


### -field D3D12_MESSAGE_CATEGORY_COMPILATION


### -field D3D12_MESSAGE_CATEGORY_STATE_CREATION


### -field D3D12_MESSAGE_CATEGORY_STATE_SETTING


### -field D3D12_MESSAGE_CATEGORY_STATE_GETTING


### -field D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION


### -field D3D12_MESSAGE_CATEGORY_EXECUTION


### -field D3D12_MESSAGE_CATEGORY_SHADER


## -remarks



This is part of the Information Queue feature, refer to the <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>
 

 

