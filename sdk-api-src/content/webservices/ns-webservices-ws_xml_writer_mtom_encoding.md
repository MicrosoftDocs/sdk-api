---
UID: NS:webservices._WS_XML_WRITER_MTOM_ENCODING
title: WS_XML_WRITER_MTOM_ENCODING (webservices.h)
description: Used to indicate that the reader should emit bytes in MTOM format. The MTOM format will represent bytes written to it as binary mime parts rather than embedded base64 encoded text.
helpviewer_keywords: ["WS_XML_WRITER_MTOM_ENCODING","WS_XML_WRITER_MTOM_ENCODING structure [Web Services for Windows]","webservices/WS_XML_WRITER_MTOM_ENCODING","wsw.ws_xml_writer_mtom_encoding"]
old-location: wsw\ws_xml_writer_mtom_encoding.htm
tech.root: wsw
ms.assetid: 18236818-492f-4906-9e7d-6ca03ef28d36
ms.date: 12/05/2018
ms.keywords: WS_XML_WRITER_MTOM_ENCODING, WS_XML_WRITER_MTOM_ENCODING structure [Web Services for Windows], webservices/WS_XML_WRITER_MTOM_ENCODING, wsw.ws_xml_writer_mtom_encoding
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
req.typenames: WS_XML_WRITER_MTOM_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_WRITER_MTOM_ENCODING
 - webservices/_WS_XML_WRITER_MTOM_ENCODING
 - WS_XML_WRITER_MTOM_ENCODING
 - webservices/WS_XML_WRITER_MTOM_ENCODING
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
 - WS_XML_WRITER_MTOM_ENCODING
---

# WS_XML_WRITER_MTOM_ENCODING structure


## -description

Used to indicate that the reader should emit bytes in MTOM format.  
        The MTOM format will represent bytes written to it as binary mime 
        parts rather than embedded base64 encoded text.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">WS_XML_WRITER_ENCODING</a>.

### -field textEncoding

Specifies the encoding of the xml document carried by MTOM.

### -field writeMimeHeader

Specifies whether or not the writer should emit a MIME header.

### -field boundary

Specifies the character sequence that should be used to delimit the mime parts.  This corresponds to the "boundary" parameter of the MIME Content-Type.

### -field startInfo

Specifies the type used by the mime part that contains the xml.  This corresponds to the "start-info" parameter in the of the MIME Content-Type.

### -field startUri

Specifies the mime part that contains the xml.  This corresponds to the "start" parameter of the MIME Content-Type.

### -field maxInlineByteCount

Specifies the threshold at which the writer will not write base64 encoded text and instead write a binary mime part for binary data.