---
UID: NS:webservices._WS_XML_READER_BUFFER_INPUT
title: WS_XML_READER_BUFFER_INPUT (webservices.h)
description: Specifies that the source of the xml input is a buffer.
helpviewer_keywords: ["WS_XML_READER_BUFFER_INPUT","WS_XML_READER_BUFFER_INPUT structure [Web Services for Windows]","webservices/WS_XML_READER_BUFFER_INPUT","wsw.ws_xml_reader_buffer_input"]
old-location: wsw\ws_xml_reader_buffer_input.htm
tech.root: wsw
ms.assetid: 86277c29-d42f-4b6a-ba33-b836bef284e7
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_BUFFER_INPUT, WS_XML_READER_BUFFER_INPUT structure [Web Services for Windows], webservices/WS_XML_READER_BUFFER_INPUT, wsw.ws_xml_reader_buffer_input
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
req.typenames: WS_XML_READER_BUFFER_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_READER_BUFFER_INPUT
 - webservices/_WS_XML_READER_BUFFER_INPUT
 - WS_XML_READER_BUFFER_INPUT
 - webservices/WS_XML_READER_BUFFER_INPUT
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
 - WS_XML_READER_BUFFER_INPUT
---

# WS_XML_READER_BUFFER_INPUT structure


## -description

Specifies that the source of the xml input is a buffer.

## -struct-fields

### -field input

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_input">WS_XML_READER_INPUT</a>.

### -field encodedData

A pointer to the bytes of data that comprise the encoded form of the xml.  The reader will not modify any of these bytes.

### -field encodedDataSize

The length of the encodedData.