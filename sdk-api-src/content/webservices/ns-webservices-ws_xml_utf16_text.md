---
UID: NS:webservices._WS_XML_UTF16_TEXT
title: WS_XML_UTF16_TEXT (webservices.h)
description: Represents text encoded as UTF-16 bytes.
helpviewer_keywords: ["WS_XML_UTF16_TEXT","WS_XML_UTF16_TEXT structure [Web Services for Windows]","webservices/WS_XML_UTF16_TEXT","wsw.ws_xml_utf16_text"]
old-location: wsw\ws_xml_utf16_text.htm
tech.root: wsw
ms.assetid: 07260aa6-4513-43e6-8803-c53199427932
ms.date: 12/05/2018
ms.keywords: WS_XML_UTF16_TEXT, WS_XML_UTF16_TEXT structure [Web Services for Windows], webservices/WS_XML_UTF16_TEXT, wsw.ws_xml_utf16_text
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
req.typenames: WS_XML_UTF16_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_UTF16_TEXT
 - webservices/_WS_XML_UTF16_TEXT
 - WS_XML_UTF16_TEXT
 - webservices/WS_XML_UTF16_TEXT
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
 - WS_XML_UTF16_TEXT
---

# WS_XML_UTF16_TEXT structure


## -description

Represents text encoded as UTF-16 bytes.

## -struct-fields

### -field text

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a>.

### -field bytes

The bytes that point to UTF-16 encoded data.

### -field byteCount

The length in bytes of the UTF-16 encoded data.