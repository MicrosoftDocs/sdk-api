---
UID: NS:webservices._WS_XML_LIST_TEXT
title: WS_XML_LIST_TEXT (webservices.h)
description: Represents a list of text values separated by a single whitespace character.
helpviewer_keywords: ["WS_XML_LIST_TEXT","WS_XML_LIST_TEXT structure [Web Services for Windows]","webservices/WS_XML_LIST_TEXT","wsw.ws_xml_list_text"]
old-location: wsw\ws_xml_list_text.htm
tech.root: wsw
ms.assetid: a9428114-6f39-46cb-b77f-9da096ed7f11
ms.date: 12/05/2018
ms.keywords: WS_XML_LIST_TEXT, WS_XML_LIST_TEXT structure [Web Services for Windows], webservices/WS_XML_LIST_TEXT, wsw.ws_xml_list_text
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
req.typenames: WS_XML_LIST_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_LIST_TEXT
 - webservices/_WS_XML_LIST_TEXT
 - WS_XML_LIST_TEXT
 - webservices/WS_XML_LIST_TEXT
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
 - WS_XML_LIST_TEXT
---

# WS_XML_LIST_TEXT structure


## -description

Represents a list of text values separated by a single whitespace character.
      

(e.g. The list { { WS_XML_TEXT_TYPE_INT32 }, 123}, 
        { { WS_XML_TEXT_TYPE_BOOL }, 1 } represents the text "123 true")

## -struct-fields

### -field text

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a>.

### -field itemCount

The number of items in the list.

### -field items

The list of items.