---
UID: NS:webservices._WS_XML_BASE64_TEXT
title: WS_XML_BASE64_TEXT (webservices.h)
description: Represents base64 encoded data.
helpviewer_keywords: ["WS_XML_BASE64_TEXT","WS_XML_BASE64_TEXT structure [Web Services for Windows]","webservices/WS_XML_BASE64_TEXT","wsw.ws_xml_base64_text"]
old-location: wsw\ws_xml_base64_text.htm
tech.root: wsw
ms.assetid: 6b4d555b-4e1f-4cc1-8204-6584a5d1dc77
ms.date: 12/05/2018
ms.keywords: WS_XML_BASE64_TEXT, WS_XML_BASE64_TEXT structure [Web Services for Windows], webservices/WS_XML_BASE64_TEXT, wsw.ws_xml_base64_text
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
req.typenames: WS_XML_BASE64_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_BASE64_TEXT
 - webservices/_WS_XML_BASE64_TEXT
 - WS_XML_BASE64_TEXT
 - webservices/WS_XML_BASE64_TEXT
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
 - WS_XML_BASE64_TEXT
---

# WS_XML_BASE64_TEXT structure


## -description

Represents base64 encoded data. (for example, the three bytes { 0, 0, 0 } represent the text "AAAA".)

## -struct-fields

### -field text

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a>.

### -field bytes

The bytes of data.

### -field length

The length of the bytes of data.