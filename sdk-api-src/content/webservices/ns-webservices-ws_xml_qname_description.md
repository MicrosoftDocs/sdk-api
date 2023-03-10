---
UID: NS:webservices._WS_XML_QNAME_DESCRIPTION
title: WS_XML_QNAME_DESCRIPTION (webservices.h)
description: This type description is used with WS_XML_QNAME_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized.
helpviewer_keywords: ["WS_XML_QNAME_DESCRIPTION","WS_XML_QNAME_DESCRIPTION structure [Web Services for Windows]","webservices/WS_XML_QNAME_DESCRIPTION","wsw.ws_xml_qname_description"]
old-location: wsw\ws_xml_qname_description.htm
tech.root: wsw
ms.assetid: 300c5fd1-1a66-40b8-9f26-0f0711f7a527
ms.date: 12/05/2018
ms.keywords: WS_XML_QNAME_DESCRIPTION, WS_XML_QNAME_DESCRIPTION structure [Web Services for Windows], webservices/WS_XML_QNAME_DESCRIPTION, wsw.ws_xml_qname_description
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_XML_QNAME_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_QNAME_DESCRIPTION
 - webservices/_WS_XML_QNAME_DESCRIPTION
 - WS_XML_QNAME_DESCRIPTION
 - webservices/WS_XML_QNAME_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_QNAME_DESCRIPTION
---

# WS_XML_QNAME_DESCRIPTION structure


## -description

This type description is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_QNAME_TYPE</a> and is optional.
                It is used to specify constraints on the set of values
                which can be deserialized.

## -struct-fields

### -field minLocalNameByteCount

The minimum number of bytes of UTF8 character data 
                    for the local name string.

### -field maxLocalNameByteCount

The maximum number of bytes of UTF8 character data
                    for the local name string.

### -field minNsByteCount

The minimum number of bytes of UTF8 character data 
                    for the namespace string.

### -field maxNsByteCount

The maximum number of bytes of UTF8 character data 
                    for the namespace string.