---
UID: NS:webservices._WS_XML_READER_BINARY_ENCODING
title: WS_XML_READER_BINARY_ENCODING (webservices.h)
description: Used to indicate that the reader should interpret the bytes it reads as binary xml.
helpviewer_keywords: ["WS_XML_READER_BINARY_ENCODING","WS_XML_READER_BINARY_ENCODING structure [Web Services for Windows]","webservices/WS_XML_READER_BINARY_ENCODING","wsw.ws_xml_reader_binary_encoding"]
old-location: wsw\ws_xml_reader_binary_encoding.htm
tech.root: wsw
ms.assetid: 51a0802b-6624-430e-96c1-a8470fac4937
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_BINARY_ENCODING, WS_XML_READER_BINARY_ENCODING structure [Web Services for Windows], webservices/WS_XML_READER_BINARY_ENCODING, wsw.ws_xml_reader_binary_encoding
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
req.typenames: WS_XML_READER_BINARY_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_READER_BINARY_ENCODING
 - webservices/_WS_XML_READER_BINARY_ENCODING
 - WS_XML_READER_BINARY_ENCODING
 - webservices/WS_XML_READER_BINARY_ENCODING
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
 - WS_XML_READER_BINARY_ENCODING
---

# WS_XML_READER_BINARY_ENCODING structure


## -description

Used to indicate that the reader should interpret the bytes it reads as binary xml.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_encoding">WS_XML_READER_ENCODING</a>.

### -field staticDictionary

Indicates the dictionary that the reader should use for static strings.  The binary representation of the xml
          document references these strings by id (as opposed to embedding the actual string), and therefore they must contain 
          the same set of strings used when the document was written.

### -field dynamicDictionary

Indicates the dictionary that the reader should use for dynamic strings. These are strings that were not in the 
          staticDictionary when the document was written but that were found by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_dynamic_string_callback">WS_DYNAMIC_STRING_CALLBACK</a>.
          The binary representation of the xml document references these strings by id (as opposed to embedding the actual string), 
          and therefore they must contain the same set of strings used when the document was written.
          The application that uses the reader and writer must coordinate communicating the values referenced by these strings.