---
UID: NS:objidlbase.tagRPCOLEMESSAGE
title: tagRPCOLEMESSAGE
author: windows-sdk-content
description: Contains marshaling invocation arguments and return values between COM components.
old-location: com\rpcolemessage.htm
old-project: com
ms.assetid: b4761462-1910-431c-b5cd-c14fdda0b6b6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PRPCOLEMESSAGE, PRPCOLEMESSAGE, PRPCOLEMESSAGE structure pointer [COM], RPCOLEMESSAGE, RPCOLEMESSAGE structure [COM], _com_RPCOLEMESSAGE, com.rpcolemessage, objidlbase/PRPCOLEMESSAGE, objidlbase/RPCOLEMESSAGE, tagRPCOLEMESSAGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidlbase.h
req.include-header: Objidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPCOLEMESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - RPCOLEMESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagRPCOLEMESSAGE structure


## -description


Contains marshaling invocation arguments and return values between COM components.


## -struct-fields




### -field reserved1

This member is reserved.


### -field dataRepresentation

The data representation with which the data was marshaled.


### -field Buffer

A buffer for marshaled data.


### -field cbBuffer

The size of the buffer, in bytes.


### -field iMethod

The number of the method to be invoked.


### -field reserved2

This member is reserved.


### -field rpcFlags

Status flags for the RPC connection.


## -see-also




<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>



<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>
 

 

