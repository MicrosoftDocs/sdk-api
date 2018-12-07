---
UID: NS:rpcdcep._RPC_MESSAGE
title: "_RPC_MESSAGE"
author: windows-sdk-content
description: The RPC_MESSAGE structure contains information shared between NDR and the rest of the RPC or OLE runtime.
old-location: rpc\rpc_message.htm
tech.root: rpc
ms.assetid: fd014622-97b3-4f76-8bc3-10821aa3c46e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRPC_MESSAGE, PRPC_MESSAGE, PRPC_MESSAGE structure pointer [RPC], RPC_MESSAGE, RPC_MESSAGE structure [RPC], _RPC_MESSAGE, rpc.rpc_message, rpcdcep/PRPC_MESSAGE, rpcdcep/RPC_MESSAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rpcdcep.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RpcdceP.h
api_name:
 - RPC_MESSAGE
product: Windows
targetos: Windows
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
req.redist: 
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

