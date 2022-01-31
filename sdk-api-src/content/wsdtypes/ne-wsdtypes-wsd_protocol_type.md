---
UID: NE:wsdtypes._WSD_PROTOCOL_TYPE
title: WSD_PROTOCOL_TYPE (wsdtypes.h)
description: Identifies the type of protocol supported by a port.
helpviewer_keywords: ["WSD_PROTOCOL_TYPE","WSD_PROTOCOL_TYPE enumeration","WSD_PT_ALL","WSD_PT_HTTP","WSD_PT_HTTPS","WSD_PT_NONE","WSD_PT_UDP","ncd.wsd_protocol_type","wsdtypes/WSD_PROTOCOL_TYPE","wsdtypes/WSD_PT_ALL","wsdtypes/WSD_PT_HTTP","wsdtypes/WSD_PT_HTTPS","wsdtypes/WSD_PT_NONE","wsdtypes/WSD_PT_UDP"]
old-location: ncd\wsd_protocol_type.htm
tech.root: ncd
ms.assetid: db18870b-2688-4d5e-8aae-7990ff0fc423
ms.date: 12/05/2018
ms.keywords: WSD_PROTOCOL_TYPE, WSD_PROTOCOL_TYPE enumeration, WSD_PT_ALL, WSD_PT_HTTP, WSD_PT_HTTPS, WSD_PT_NONE, WSD_PT_UDP, ncd.wsd_protocol_type, wsdtypes/WSD_PROTOCOL_TYPE, wsdtypes/WSD_PT_ALL, wsdtypes/WSD_PT_HTTP, wsdtypes/WSD_PT_HTTPS, wsdtypes/WSD_PT_NONE, wsdtypes/WSD_PT_UDP
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
req.typenames: WSD_PROTOCOL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PROTOCOL_TYPE
 - wsdtypes/_WSD_PROTOCOL_TYPE
 - WSD_PROTOCOL_TYPE
 - wsdtypes/WSD_PROTOCOL_TYPE
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
 - WSD_PROTOCOL_TYPE
---

# WSD_PROTOCOL_TYPE enumeration


## -description

Identifies the type of protocol supported by a port.

## -enum-fields

### -field WSD_PT_NONE:0x00

No protocols supported.

### -field WSD_PT_UDP:0x01

The UDP protocol is supported.

### -field WSD_PT_HTTP:0x02

The HTTP protocol is supported.

### -field WSD_PT_HTTPS:0x04

The HTTPS protocol is supported.

### -field WSD_PT_ALL:0xff

The UDP, HTTP, and HTTPS protocols are supported.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_port_type">WSD_PORT_TYPE</a>
