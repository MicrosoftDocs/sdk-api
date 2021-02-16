---
UID: NS:webservices._WS_XML_DOUBLE_TEXT
title: WS_XML_DOUBLE_TEXT (webservices.h)
description: Represents an 8 byte floating point value.
helpviewer_keywords: ["WS_XML_DOUBLE_TEXT","WS_XML_DOUBLE_TEXT structure [Web Services for Windows]","webservices/WS_XML_DOUBLE_TEXT","wsw.ws_xml_double_text"]
old-location: wsw\ws_xml_double_text.htm
tech.root: wsw
ms.assetid: dff0aceb-7588-47e2-9ca0-dfa58eb25001
ms.date: 12/05/2018
ms.keywords: WS_XML_DOUBLE_TEXT, WS_XML_DOUBLE_TEXT structure [Web Services for Windows], webservices/WS_XML_DOUBLE_TEXT, wsw.ws_xml_double_text
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
req.typenames: WS_XML_DOUBLE_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_DOUBLE_TEXT
 - webservices/_WS_XML_DOUBLE_TEXT
 - WS_XML_DOUBLE_TEXT
 - webservices/WS_XML_DOUBLE_TEXT
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
 - WS_XML_DOUBLE_TEXT
---

# WS_XML_DOUBLE_TEXT structure


## -description

Represents an 8 byte floating point value.  (e.g. The value 0.0 represents the text "0")

## -struct-fields

### -field text

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a>.

### -field value

The value.

## -remarks

The textual representation of the value has enough digits to preserve the floating point value.
      

Negative zero is represented by the text "-0".
      

Positive infinity is represented by the text "INF";
      

Negative infinity is represented by the text "-INF";
      

Unrepresentable values are represented by the text "NaN".
      

For more information on this representation, refer to IEEE Standard for Binary Floating-Point Arithmetic, available on the Web site http://www.ieee.org/.