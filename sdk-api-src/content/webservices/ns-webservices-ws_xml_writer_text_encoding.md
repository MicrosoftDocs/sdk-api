---
UID: NS:webservices._WS_XML_WRITER_TEXT_ENCODING
title: WS_XML_WRITER_TEXT_ENCODING (webservices.h)
description: Indicates that the reader should emit bytes as textual xml.
helpviewer_keywords: ["WS_XML_WRITER_TEXT_ENCODING","WS_XML_WRITER_TEXT_ENCODING structure [Web Services for Windows]","webservices/WS_XML_WRITER_TEXT_ENCODING","wsw.ws_xml_writer_text_encoding"]
old-location: wsw\ws_xml_writer_text_encoding.htm
tech.root: wsw
ms.assetid: 916e693b-9804-4c93-869d-0c3b576e5b61
ms.date: 12/05/2018
ms.keywords: WS_XML_WRITER_TEXT_ENCODING, WS_XML_WRITER_TEXT_ENCODING structure [Web Services for Windows], webservices/WS_XML_WRITER_TEXT_ENCODING, wsw.ws_xml_writer_text_encoding
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
req.typenames: WS_XML_WRITER_TEXT_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_WRITER_TEXT_ENCODING
 - webservices/_WS_XML_WRITER_TEXT_ENCODING
 - WS_XML_WRITER_TEXT_ENCODING
 - webservices/WS_XML_WRITER_TEXT_ENCODING
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
 - WS_XML_WRITER_TEXT_ENCODING
---

# WS_XML_WRITER_TEXT_ENCODING structure


## -description

Indicates that the reader should emit bytes as textual xml.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">WS_XML_WRITER_ENCODING</a>.

### -field charSet

Indicates the text encoding of the bytes.  This may not be <a href="/windows/desktop/api/webservices/ne-webservices-ws_charset">WS_CHARSET_AUTO</a>.