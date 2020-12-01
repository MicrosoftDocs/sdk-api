---
UID: NS:webservices._WS_XML_READER_RAW_ENCODING
title: WS_XML_READER_RAW_ENCODING (webservices.h)
description: Used to indicate that the reader should surface the bytes of the document as base64 encoded characters.
helpviewer_keywords: ["WS_XML_READER_RAW_ENCODING","WS_XML_READER_RAW_ENCODING structure [Web Services for Windows]","webservices/WS_XML_READER_RAW_ENCODING","wsw.ws_xml_reader_raw_encoding"]
old-location: wsw\ws_xml_reader_raw_encoding.htm
tech.root: wsw
ms.assetid: 5f3004e7-347f-46a5-8d8f-743a76e1fa71
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_RAW_ENCODING, WS_XML_READER_RAW_ENCODING structure [Web Services for Windows], webservices/WS_XML_READER_RAW_ENCODING, wsw.ws_xml_reader_raw_encoding
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
req.typenames: WS_XML_READER_RAW_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_READER_RAW_ENCODING
 - webservices/_WS_XML_READER_RAW_ENCODING
 - WS_XML_READER_RAW_ENCODING
 - webservices/WS_XML_READER_RAW_ENCODING
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
 - WS_XML_READER_RAW_ENCODING
---

# WS_XML_READER_RAW_ENCODING structure


## -description

Used to indicate that the reader should surface the bytes of the document as base64 encoded characters.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_encoding">WS_XML_READER_ENCODING</a>.

## -remarks

This encoding can be useful when it is desirable to read an arbitrary, perhaps, non-xml document
        while still using the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> abstraction.  In this encoding, the bytes comprising
        the document are presented as base64 encoded characters at the root of a xml document.  In order to
        accommodate non-whitespace text at the root of the document, the reader will operate as if the
        <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_reader_property_id">WS_XML_READER_PROPERTY_ALLOW_FRAGMENT</a> property has been specified.
      

The bytes of the document are only converted to base64 when necessary.  So, for example, using 
        <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbytes">WsReadBytes</a>, which normally performs a base64 decoding of the characters it reads, 
        actually avoids all base64 conversions and is the most efficient way to read documents in this
        encoding. Using <a href="/windows/desktop/api/webservices/nf-webservices-wsreadchars">WsReadChars</a>, for example, will cause the bytes to physically get 
        converted to their corresponding base64 characters.  In general reading the document using
        anything other than <b>WsReadBytes</b> will incur the base64 conversion.