---
UID: NS:webservices._WS_XML_ATTRIBUTE
title: WS_XML_ATTRIBUTE (webservices.h)
description: Represents an attribute (for example, &lt;a:purchaseOrder xmlns:a=&quot;http://tempuri.org&quot; id=&quot;5&quot;&gt;)
helpviewer_keywords: ["WS_XML_ATTRIBUTE","WS_XML_ATTRIBUTE structure [Web Services for Windows]","webservices/WS_XML_ATTRIBUTE","wsw.ws_xml_attribute"]
old-location: wsw\ws_xml_attribute.htm
tech.root: wsw
ms.assetid: 338c31ac-d5eb-4d2d-8ee1-953963c1a8b0
ms.date: 12/05/2018
ms.keywords: WS_XML_ATTRIBUTE, WS_XML_ATTRIBUTE structure [Web Services for Windows], webservices/WS_XML_ATTRIBUTE, wsw.ws_xml_attribute
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
req.typenames: WS_XML_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_ATTRIBUTE
 - webservices/_WS_XML_ATTRIBUTE
 - WS_XML_ATTRIBUTE
 - webservices/WS_XML_ATTRIBUTE
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
 - WS_XML_ATTRIBUTE
---

# WS_XML_ATTRIBUTE structure


## -description

Represents an attribute (for example, &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)

## -struct-fields

### -field singleQuote

Whether to use a single quote or double quote to surround an attribute value.  In the example, the value of singleQuote for attribute "id" would be <b>FALSE</b>.

### -field isXmlNs

Whether or not the attribute is an xmlns attribute.  In the example above, this would be <b>TRUE</b> for the attribute "xmlns:a", but <b>FALSE</b> for the attribute "id".

### -field prefix

The prefix of the attribute.  In the example above, the prefix for attribute "xmlns:a" is "a", while the prefix for "id" is a zero length string.
        

The prefix for the attribute "xmlns" is a zero length string.

### -field localName

The localName of the attribute.  In the example above, the localName for attribute "xmlns:a" is not used so it is <b>NULL</b>.  The localName for attribute "id" is "id".

### -field ns

The namespace of the attribute.  In the example above, the namespace for the attribute "xmlns:a" is "http://tempuri.org".  The namespace for attribute "id" is the
          empty namespace which is represented by a zero length string.

### -field value

The value of the attribute.  In the example above the value for attribute "xmlns:a" is not used so it is <b>NULL</b>.  The value for the attribute "id" is a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text">WS_XML_TEXT</a> that refers to the value "5".