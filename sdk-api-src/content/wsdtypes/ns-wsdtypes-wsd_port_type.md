---
UID: NS:wsdtypes._WSD_PORT_TYPE
title: WSD_PORT_TYPE (wsdtypes.h)
description: Supplies data about a port type.
helpviewer_keywords: ["WSD_PORT_TYPE","WSD_PORT_TYPE structure","ncd.wsd_port_type_struct","wsdtypes/WSD_PORT_TYPE"]
old-location: ncd\wsd_port_type_struct.htm
tech.root: ncd
ms.assetid: ec321771-b3d1-4e7b-b870-009db7c49c6e
ms.date: 12/05/2018
ms.keywords: WSD_PORT_TYPE, WSD_PORT_TYPE structure, ncd.wsd_port_type_struct, wsdtypes/WSD_PORT_TYPE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSD_PORT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PORT_TYPE
 - wsdtypes/_WSD_PORT_TYPE
 - WSD_PORT_TYPE
 - wsdtypes/WSD_PORT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_PORT_TYPE
---

# WSD_PORT_TYPE structure


## -description

Supplies data about a port type. This structure is populated by <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a>.

## -struct-fields

### -field EncodedName

The encoded qualified name of the port type.

### -field OperationCount

The number of operations in the array referenced by the <b>Operations</b> member.

### -field Operations

Reference to an array of <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structures that specifies the operations comprising the port type.

### -field ProtocolType

A <a href="/windows/desktop/api/wsdtypes/ne-wsdtypes-wsd_protocol_type">WSD_PROTOCOL_TYPE</a> value that specifies the protocol(s) supported by the port type.