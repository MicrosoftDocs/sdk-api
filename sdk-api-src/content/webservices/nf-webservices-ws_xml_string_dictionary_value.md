---
UID: NF:webservices.WS_XML_STRING_DICTIONARY_VALUE
title: WS_XML_STRING_DICTIONARY_VALUE macro (webservices.h)
description: Provides an initializer for a WS_XML_STRING structure when there is an associated dictionary ID.
helpviewer_keywords: ["WS_XML_STRING_DICTIONARY_VALUE","WS_XML_STRING_DICTIONARY_VALUE function [Web Services for Windows]","webservices/WS_XML_STRING_DICTIONARY_VALUE","wsw.ws_xml_string_dictionary_value"]
old-location: wsw\ws_xml_string_dictionary_value.htm
tech.root: wsw
ms.assetid: 1e2045c0-11c5-4369-9b82-dc759eb1412e
ms.date: 12/05/2018
ms.keywords: WS_XML_STRING_DICTIONARY_VALUE, WS_XML_STRING_DICTIONARY_VALUE function [Web Services for Windows], webservices/WS_XML_STRING_DICTIONARY_VALUE, wsw.ws_xml_string_dictionary_value
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_STRING_DICTIONARY_VALUE
 - webservices/WS_XML_STRING_DICTIONARY_VALUE
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
 - WS_XML_STRING_DICTIONARY_VALUE
---

# WS_XML_STRING_DICTIONARY_VALUE macro


## -description

Provides an initializer for a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> structure when there is an associated dictionary ID.

## -parameters

### -param S

A static constant string, encoded in UTF-8.

### -param D

A string dictionary.

### -param I

The ID.

## -remarks

This initializer assumes the string is a static constant string.  It must be encoded in UTF-8.
      

The following is example usage:
      

<code>WS_XML_STRING myString = WS_XML_STRING_DICTIONARY_VALUE("MyString", myDictionary, 5);</code>