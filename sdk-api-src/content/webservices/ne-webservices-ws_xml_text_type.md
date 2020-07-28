---
UID: NE:webservices.__unnamed_enum_5
title: WS_XML_TEXT_TYPE (webservices.h)
description: The type of WS_XML_TEXT structure.
helpviewer_keywords: ["WS_XML_TEXT_TYPE","WS_XML_TEXT_TYPE enumeration [Web Services for Windows]","WS_XML_TEXT_TYPE_BASE64","WS_XML_TEXT_TYPE_BOOL","WS_XML_TEXT_TYPE_DATETIME","WS_XML_TEXT_TYPE_DECIMAL","WS_XML_TEXT_TYPE_DOUBLE","WS_XML_TEXT_TYPE_FLOAT","WS_XML_TEXT_TYPE_GUID","WS_XML_TEXT_TYPE_INT32","WS_XML_TEXT_TYPE_INT64","WS_XML_TEXT_TYPE_LIST","WS_XML_TEXT_TYPE_QNAME","WS_XML_TEXT_TYPE_TIMESPAN","WS_XML_TEXT_TYPE_UINT64","WS_XML_TEXT_TYPE_UNIQUE_ID","WS_XML_TEXT_TYPE_UTF16","WS_XML_TEXT_TYPE_UTF8","webservices/WS_XML_TEXT_TYPE","webservices/WS_XML_TEXT_TYPE_BASE64","webservices/WS_XML_TEXT_TYPE_BOOL","webservices/WS_XML_TEXT_TYPE_DATETIME","webservices/WS_XML_TEXT_TYPE_DECIMAL","webservices/WS_XML_TEXT_TYPE_DOUBLE","webservices/WS_XML_TEXT_TYPE_FLOAT","webservices/WS_XML_TEXT_TYPE_GUID","webservices/WS_XML_TEXT_TYPE_INT32","webservices/WS_XML_TEXT_TYPE_INT64","webservices/WS_XML_TEXT_TYPE_LIST","webservices/WS_XML_TEXT_TYPE_QNAME","webservices/WS_XML_TEXT_TYPE_TIMESPAN","webservices/WS_XML_TEXT_TYPE_UINT64","webservices/WS_XML_TEXT_TYPE_UNIQUE_ID","webservices/WS_XML_TEXT_TYPE_UTF16","webservices/WS_XML_TEXT_TYPE_UTF8","wsw.ws_xml_text_type"]
old-location: wsw\ws_xml_text_type.htm
tech.root: wsw
ms.assetid: 8c7695b9-7593-4d00-85d1-fbb7778d959a
ms.date: 12/05/2018
ms.keywords: WS_XML_TEXT_TYPE, WS_XML_TEXT_TYPE enumeration [Web Services for Windows], WS_XML_TEXT_TYPE_BASE64, WS_XML_TEXT_TYPE_BOOL, WS_XML_TEXT_TYPE_DATETIME, WS_XML_TEXT_TYPE_DECIMAL, WS_XML_TEXT_TYPE_DOUBLE, WS_XML_TEXT_TYPE_FLOAT, WS_XML_TEXT_TYPE_GUID, WS_XML_TEXT_TYPE_INT32, WS_XML_TEXT_TYPE_INT64, WS_XML_TEXT_TYPE_LIST, WS_XML_TEXT_TYPE_QNAME, WS_XML_TEXT_TYPE_TIMESPAN, WS_XML_TEXT_TYPE_UINT64, WS_XML_TEXT_TYPE_UNIQUE_ID, WS_XML_TEXT_TYPE_UTF16, WS_XML_TEXT_TYPE_UTF8, webservices/WS_XML_TEXT_TYPE, webservices/WS_XML_TEXT_TYPE_BASE64, webservices/WS_XML_TEXT_TYPE_BOOL, webservices/WS_XML_TEXT_TYPE_DATETIME, webservices/WS_XML_TEXT_TYPE_DECIMAL, webservices/WS_XML_TEXT_TYPE_DOUBLE, webservices/WS_XML_TEXT_TYPE_FLOAT, webservices/WS_XML_TEXT_TYPE_GUID, webservices/WS_XML_TEXT_TYPE_INT32, webservices/WS_XML_TEXT_TYPE_INT64, webservices/WS_XML_TEXT_TYPE_LIST, webservices/WS_XML_TEXT_TYPE_QNAME, webservices/WS_XML_TEXT_TYPE_TIMESPAN, webservices/WS_XML_TEXT_TYPE_UINT64, webservices/WS_XML_TEXT_TYPE_UNIQUE_ID, webservices/WS_XML_TEXT_TYPE_UTF16, webservices/WS_XML_TEXT_TYPE_UTF8, wsw.ws_xml_text_type
f1_keywords:
- webservices/WS_XML_TEXT_TYPE
dev_langs:
- c++
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WebServices.h
api_name:
- WS_XML_TEXT_TYPE
targetos: Windows
req.typenames: WS_XML_TEXT_TYPE
req.redist: 
ms.custom: 19H1
---

# WS_XML_TEXT_TYPE enumeration


## -description


The type of <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a> structure.
      


## -enum-fields




### -field WS_XML_TEXT_TYPE_UTF8

Characters encoded as UTF-8 bytes.
        


### -field WS_XML_TEXT_TYPE_UTF16

Characters encoded as UTF-16 bytes.
        


### -field WS_XML_TEXT_TYPE_BASE64

Bytes that represent base64 encoded text.
        


### -field WS_XML_TEXT_TYPE_BOOL

A Boolean value that represents the text "true" or "false"
        


### -field WS_XML_TEXT_TYPE_INT32

A signed 32 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_INT64

A signed 64 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_UINT64

An unsigned 64 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_FLOAT

An 4 byte floating point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_DOUBLE

An 8 byte floating point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_DECIMAL

A 12 byte fixed point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_GUID

A GUID that represents the text "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx".
        


### -field WS_XML_TEXT_TYPE_UNIQUE_ID

A GUID that represents the text "urn:uuid:xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx".
        


### -field WS_XML_TEXT_TYPE_DATETIME

A datetime.
        


### -field WS_XML_TEXT_TYPE_TIMESPAN

A timespan.
        


### -field WS_XML_TEXT_TYPE_QNAME

A qualified name.
        


### -field WS_XML_TEXT_TYPE_LIST

A list of values that represent their text forms separated by a single whitespace character.
        

