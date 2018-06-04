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

# D3D10_MESSAGE_SEVERITY enumeration


## -description


Debug message severity levels for an information queue.


## -enum-fields




### -field D3D10_MESSAGE_SEVERITY_CORRUPTION

Defines some type of corruption which has occurred.


### -field D3D10_MESSAGE_SEVERITY_ERROR

Defines an error message.


### -field D3D10_MESSAGE_SEVERITY_WARNING

Defines a warning message.


### -field D3D10_MESSAGE_SEVERITY_INFO

Defines an information message.


### -field D3D10_MESSAGE_SEVERITY_MESSAGE




## -remarks



Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">D3D10_INFO_QUEUE_FILTER</a>). This API is used by <a href="https://msdn.microsoft.com/223f9a01-4507-4877-bd86-c5b9cb441d7a">ID3D10InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

