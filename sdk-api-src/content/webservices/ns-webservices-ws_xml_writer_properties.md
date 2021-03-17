---
UID: NS:webservices._WS_XML_WRITER_PROPERTIES
title: WS_XML_WRITER_PROPERTIES (webservices.h)
description: A structure that is used to specify a set of WS_XML_WRITER_PROPERTYs.
helpviewer_keywords: ["WS_XML_WRITER_PROPERTIES","WS_XML_WRITER_PROPERTIES structure [Web Services for Windows]","webservices/WS_XML_WRITER_PROPERTIES","wsw.ws_xml_writer_properties"]
old-location: wsw\ws_xml_writer_properties.htm
tech.root: wsw
ms.assetid: 8c874422-3d59-43cd-b65e-8f4f543e57e5
ms.date: 12/05/2018
ms.keywords: WS_XML_WRITER_PROPERTIES, WS_XML_WRITER_PROPERTIES structure [Web Services for Windows], webservices/WS_XML_WRITER_PROPERTIES, wsw.ws_xml_writer_properties
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
req.typenames: WS_XML_WRITER_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_WRITER_PROPERTIES
 - webservices/_WS_XML_WRITER_PROPERTIES
 - WS_XML_WRITER_PROPERTIES
 - webservices/WS_XML_WRITER_PROPERTIES
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
 - WS_XML_WRITER_PROPERTIES
---

# WS_XML_WRITER_PROPERTIES structure


## -description

A structure that is used to specify a set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_property">WS_XML_WRITER_PROPERTY</a>s.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
                   using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                   is 0.

### -field propertyCount

The number of elements in the properties array.