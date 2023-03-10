---
UID: NS:webservices._WS_XML_READER_MTOM_ENCODING
title: WS_XML_READER_MTOM_ENCODING (webservices.h)
description: Used to indicate that the reader should interpret the bytes it reads as in MTOM format.
helpviewer_keywords: ["WS_XML_READER_MTOM_ENCODING","WS_XML_READER_MTOM_ENCODING structure [Web Services for Windows]","webservices/WS_XML_READER_MTOM_ENCODING","wsw.ws_xml_reader_mtom_encoding"]
old-location: wsw\ws_xml_reader_mtom_encoding.htm
tech.root: wsw
ms.assetid: dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_MTOM_ENCODING, WS_XML_READER_MTOM_ENCODING structure [Web Services for Windows], webservices/WS_XML_READER_MTOM_ENCODING, wsw.ws_xml_reader_mtom_encoding
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
req.typenames: WS_XML_READER_MTOM_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_READER_MTOM_ENCODING
 - webservices/_WS_XML_READER_MTOM_ENCODING
 - WS_XML_READER_MTOM_ENCODING
 - webservices/WS_XML_READER_MTOM_ENCODING
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
 - WS_XML_READER_MTOM_ENCODING
---

# WS_XML_READER_MTOM_ENCODING structure


## -description

Used to indicate that the reader should interpret the bytes it reads as in MTOM format.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_encoding">WS_XML_READER_ENCODING</a>.

### -field textEncoding

The encoding of the xml document carried by MTOM.

### -field readMimeHeader

Specifies whether or not the reader should read the MIME header.

### -field startInfo

The type used by the mime part that contains the xml.  This corresponds to the "start-info" parameter in the of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the startInfo will be read from the mime header.

### -field boundary

The character sequence that should be used to delimit the mime parts.  This corresponds to the "boundary" parameter of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the boundary will be read from the mime header.

### -field startUri

The mime part that contains the xml.  This corresponds to the "start" parameter of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the startUri will be read from the mime header.

## -remarks

When used with <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_buffer_input">WS_XML_READER_BUFFER_INPUT</a> the MIME parts may appear in any order.
      

When used with <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_stream_input">WS_XML_READER_STREAM_INPUT</a> the root MIME part must be first, and
        subsequent MIME parts must appear in the order that they are referenced from xop:Include elements.
      

See http://www.w3.org/TR/2005/REC-xop10-20050125/ for the MTOM specification.