---
UID: NS:webservices._WS_XML_WRITER_BINARY_ENCODING
title: WS_XML_WRITER_BINARY_ENCODING (webservices.h)
description: Used to indicate that the writer should emit bytes as binary xml.
helpviewer_keywords: ["WS_XML_WRITER_BINARY_ENCODING","WS_XML_WRITER_BINARY_ENCODING structure [Web Services for Windows]","webservices/WS_XML_WRITER_BINARY_ENCODING","wsw.ws_xml_writer_binary_encoding"]
old-location: wsw\ws_xml_writer_binary_encoding.htm
tech.root: wsw
ms.assetid: b4485490-b5e1-406c-883c-a30bfa334316
ms.date: 12/05/2018
ms.keywords: WS_XML_WRITER_BINARY_ENCODING, WS_XML_WRITER_BINARY_ENCODING structure [Web Services for Windows], webservices/WS_XML_WRITER_BINARY_ENCODING, wsw.ws_xml_writer_binary_encoding
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
req.typenames: WS_XML_WRITER_BINARY_ENCODING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_WRITER_BINARY_ENCODING
 - webservices/_WS_XML_WRITER_BINARY_ENCODING
 - WS_XML_WRITER_BINARY_ENCODING
 - webservices/WS_XML_WRITER_BINARY_ENCODING
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
 - WS_XML_WRITER_BINARY_ENCODING
---

# WS_XML_WRITER_BINARY_ENCODING structure


## -description

Used to indicate that the writer should emit bytes as binary xml.

## -struct-fields

### -field encoding

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">WS_XML_WRITER_ENCODING</a>.

### -field staticDictionary

Indicates the dictionary that the writer should use for static strings.  <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a>s that are written that
          reference this dictionary, will be written in the binary xml document using an id rather than the string itself.
          When reading this document, the application must provide a dictionary with the same strings.

### -field dynamicStringCallback

Specifies an optional callback that the writer will invoke when a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> that is not found in the staticDictionary is written for the first time.
          The callback provides the mapping to an id which the writer will then use.  It is the responsibility of the callback to coordinate with the
          writer to propagate these strings to the reader. The string is not added to the dictionary if this callback is not specified.

### -field dynamicStringCallbackState

User-defined state that will be passed to dynamicStringCallback.