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

# D3D11_MESSAGE_SEVERITY enumeration


## -description


Debug message severity levels for an information queue.


## -enum-fields




### -field D3D11_MESSAGE_SEVERITY_CORRUPTION

Defines some type of corruption which has occurred.


### -field D3D11_MESSAGE_SEVERITY_ERROR

Defines an error message.


### -field D3D11_MESSAGE_SEVERITY_WARNING

Defines a warning message.


### -field D3D11_MESSAGE_SEVERITY_INFO

Defines an information message.


### -field D3D11_MESSAGE_SEVERITY_MESSAGE

Defines a message other than corruption, error, warning, or information.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -remarks



Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">D3D11_INFO_QUEUE_FILTER</a>). This API is used by <a href="https://msdn.microsoft.com/ca5a5e33-f912-4283-8b23-b212ace6089c">ID3D11InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Layer Enumerations</a>
 

 

