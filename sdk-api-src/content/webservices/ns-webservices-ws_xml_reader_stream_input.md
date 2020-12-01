---
UID: NS:webservices._WS_XML_READER_STREAM_INPUT
title: WS_XML_READER_STREAM_INPUT (webservices.h)
description: Specifies that the source of the xml should be obtained from a callback.
helpviewer_keywords: ["WS_XML_READER_STREAM_INPUT","WS_XML_READER_STREAM_INPUT structure [Web Services for Windows]","webservices/WS_XML_READER_STREAM_INPUT","wsw.ws_xml_reader_stream_input"]
old-location: wsw\ws_xml_reader_stream_input.htm
tech.root: wsw
ms.assetid: 53537eb2-6b8d-443e-9453-4b39dfef1dd7
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_STREAM_INPUT, WS_XML_READER_STREAM_INPUT structure [Web Services for Windows], webservices/WS_XML_READER_STREAM_INPUT, wsw.ws_xml_reader_stream_input
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
req.typenames: WS_XML_READER_STREAM_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_READER_STREAM_INPUT
 - webservices/_WS_XML_READER_STREAM_INPUT
 - WS_XML_READER_STREAM_INPUT
 - webservices/WS_XML_READER_STREAM_INPUT
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
 - WS_XML_READER_STREAM_INPUT
---

# WS_XML_READER_STREAM_INPUT structure


## -description

Specifies that the source of the xml should be obtained from a callback.

## -struct-fields

### -field input

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_input">WS_XML_READER_INPUT</a>.

### -field readCallback

A callback that is invoked when <a href="/windows/desktop/api/webservices/nf-webservices-wsfillreader">WsFillReader</a> is called.

### -field readCallbackState

A user-defined value that will be passed back to readCallback.