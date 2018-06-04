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

# _WSD_PORT_TYPE structure


## -description


Supplies data about a port type. This structure is populated by <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a>.


## -struct-fields




### -field EncodedName

The encoded qualified name of the port type.


### -field OperationCount

The number of operations in the array referenced by the <b>Operations</b> member.


### -field Operations

Reference to an array of <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structures that specifies the operations comprising the port type.


### -field ProtocolType

A <a href="https://msdn.microsoft.com/db18870b-2688-4d5e-8aae-7990ff0fc423">WSD_PROTOCOL_TYPE</a> value that specifies the protocol(s) supported by the port type.

