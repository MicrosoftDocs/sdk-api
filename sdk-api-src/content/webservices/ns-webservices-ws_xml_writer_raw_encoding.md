---
UID: NS:webservices._WS_XML_WRITER_RAW_ENCODING
title: WS_XML_WRITER_RAW_ENCODING (webservices.h)
description: Used to indicate that the writer should emit bytes from decoded base64 characters.
helpviewer_keywords: ["WS_XML_WRITER_RAW_ENCODING","WS_XML_WRITER_RAW_ENCODING structure [Web Services for Windows]","webservices/WS_XML_WRITER_RAW_ENCODING","wsw.ws_xml_writer_raw_encoding"]
old-location: wsw\ws_xml_writer_raw_encoding.htm
tech.root: wsw
ms.assetid: 655a7d13-8ef1-4863-a6a2-4636ba0a8983
ms.date: 12/05/2018
ms.keywords: WS_XML_WRITER_RAW_ENCODING, WS_XML_WRITER_RAW_ENCODING structure [Web Services for Windows], webservices/WS_XML_WRITER_RAW_ENCODING, wsw.ws_xml_writer_raw_encoding
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
req.typenames: WS_XML_WRITER_RAW_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_WRITER_RAW_ENCODING
 - webservices/_WS_XML_WRITER_RAW_ENCODING
 - WS_XML_WRITER_RAW_ENCODING
 - webservices/WS_XML_WRITER_RAW_ENCODING
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
 - WS_XML_WRITER_RAW_ENCODING
---

# WS_XML_WRITER_RAW_ENCODING structure


## -description

Used to indicate that the writer should emit bytes from decoded base64 characters.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">WS_XML_WRITER_ENCODING</a>.

## -remarks

This encoding can be useful when it is desirable to write an arbitrary, perhaps, non-xml document
        while still using the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> abstraction.  In this encoding, only characters
        representing base64 encoded bytes may be written, and only at the root of the document.  No
        elements or comments may be written.  The writer will emit the bytes represented by the base64 encoded 
        characters.  In order to accommodate non-whitespace text at the root of the document, the writer 
        will operate as if the <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</a> property has been specified.
      

The base64 characters of the document are only converted to bytes when necessary.  So, for example, 
        using <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a>, which normally performs a base64 encoding of the bytes it is passed,
        actually avoids all base64 conversions and is the most efficient way to write documents in this
        encoding. Using <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>, for example, will cause the base64 characters to physically get
        decoded to their corresponding bytes.  In general writing the document using anything other than 
        <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbytes">WsReadBytes</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wspullbytes">WsPullBytes</a>, or <a href="/windows/desktop/api/webservices/nf-webservices-wspushbytes">WsPushBytes</a> will incur the 
        base64 conversion.