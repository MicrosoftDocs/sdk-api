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

# _WSD_EVENT structure


## -description


Provides an internal representation of a SOAP message.


## -struct-fields




### -field Hr

The result code of the event.


### -field EventType

The event type.


### -field DispatchTag

Pointer to the protocol string when dispatch by tags is required.


### -field HandlerContext

Reference to a <a href="https://msdn.microsoft.com/d7b69627-5847-47ec-8ada-2df9b427e870">WSD_HANDLER_CONTEXT</a> structure that specifies the handler context.


### -field Soap

Reference to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that describes the event.


### -field Operation

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation performed.


### -field MessageParameters

Message transmission parameters.

