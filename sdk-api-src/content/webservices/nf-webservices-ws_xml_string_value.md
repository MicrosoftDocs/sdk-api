---
UID: NF:webservices.WS_XML_STRING_VALUE
title: WS_XML_STRING_VALUE macro (webservices.h)
description: Provides an initializer for a WS_XML_STRING structure when there is no associated dictionary ID.helpviewer_keywords: ["WS_XML_STRING_VALUE","WS_XML_STRING_VALUE macro [Web Services for Windows]","webservices/WS_XML_STRING_VALUE","wsw.ws_xml_string_value"]
old-location: wsw\ws_xml_string_value.htm
tech.root: wsw
ms.assetid: 95e2326c-d4b2-421c-b991-ca9c332b6f6f
ms.date: 12/05/2018
ms.keywords: WS_XML_STRING_VALUE, WS_XML_STRING_VALUE macro [Web Services for Windows], webservices/WS_XML_STRING_VALUE, wsw.ws_xml_string_value
f1_keywords:
- webservices/WS_XML_STRING_VALUE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WebServices.h
api_name:
- WS_XML_STRING_VALUE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WS_XML_STRING_VALUE macro


## -description


Provides an initializer for a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> structure when there is no associated dictionary ID.
      


## -parameters




### -param S

A static constant string, encoded in UTF-8.






## -remarks



This initializer assumes the string is a static constant string.  It must be encoded in UTF-8.
      

The following is example usage:
      

<code>WS_XML_STRING myString = WS_XML_STRING_VALUE("MyString");</code>



