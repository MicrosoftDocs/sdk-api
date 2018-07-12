---
UID: NS:wsdtypes._WSD_PORT_TYPE
title: "_WSD_PORT_TYPE"
author: windows-sdk-content
description: Supplies data about a port type.
old-location: ncd\wsd_port_type_struct.htm
old-project: wsdapi
ms.assetid: ec321771-b3d1-4e7b-b870-009db7c49c6e
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: WSD_PORT_TYPE, WSD_PORT_TYPE structure, _WSD_PORT_TYPE, ncd.wsd_port_type_struct, wsdtypes/WSD_PORT_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_PORT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_PORT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

