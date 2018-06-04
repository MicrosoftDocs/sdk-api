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

# _RPC_MESSAGE structure


## -description


The <b>RPC_MESSAGE</b> structure contains information shared between NDR and the rest of the RPC or OLE runtime.


## -struct-fields




### -field Handle

Reserved.


### -field DataRepresentation

Data representation of the network buffer as defined by the NDR specification.


### -field Buffer

Pointer to the beginning of the network buffer.


### -field BufferLength

Size, in bytes, of <b>Buffer</b>.


### -field ProcNum

Reserved.


### -field TransferSyntax

Reserved.


### -field RpcInterfaceInformation

Reserved.


### -field ReservedForRuntime

Reserved.


### -field ManagerEpv

Reserved.


### -field ImportContext

Reserved.


### -field RpcFlags

Reserved.

