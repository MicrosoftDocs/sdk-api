---
UID: NS:wsdtypes._WSD_HELLO
title: WSD_HELLO (wsdtypes.h)
description: Represents a Hello message.
helpviewer_keywords: ["WSD_HELLO","WSD_HELLO structure","ncd.wsd_hello_struct","wsdtypes/WSD_HELLO"]
old-location: ncd\wsd_hello_struct.htm
tech.root: ncd
ms.assetid: 71fad98a-d115-4350-b3aa-3f3927b2c24d
ms.date: 12/05/2018
ms.keywords: WSD_HELLO, WSD_HELLO structure, ncd.wsd_hello_struct, wsdtypes/WSD_HELLO
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
req.typenames: WSD_HELLO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_HELLO
 - wsdtypes/_WSD_HELLO
 - WSD_HELLO
 - wsdtypes/WSD_HELLO
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
 - WSD_HELLO
---

# WSD_HELLO structure


## -description

Represents a <a href="/windows/desktop/WsdApi/hello-message">Hello</a> message.

## -struct-fields

### -field EndpointReference

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint announcing the Hello message.

### -field Types

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.

### -field Scopes

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_scopes">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.

### -field XAddrs

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that contains a list of WS-Discovery XAddrs.

### -field MetadataVersion

The metadata version of this message.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/hello-message">Hello Message</a>