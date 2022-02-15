---
UID: NE:webservices.__unnamed_enum_1
title: WS_XML_CANONICALIZATION_ALGORITHM (webservices.h)
description: The values for the XML canonicalization algorithms.
helpviewer_keywords: ["WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM","WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM","WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM","WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM","WS_XML_CANONICALIZATION_ALGORITHM","WS_XML_CANONICALIZATION_ALGORITHM enumeration [Web Services for Windows]","webservices/WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM","webservices/WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM","webservices/WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM","webservices/WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM","webservices/WS_XML_CANONICALIZATION_ALGORITHM","wsw.ws_xml_canonicalization_algorithm"]
old-location: wsw\ws_xml_canonicalization_algorithm.htm
tech.root: wsw
ms.assetid: 230e4b9d-f6ce-45a8-9efd-2a6949d3e6f4
ms.date: 12/05/2018
ms.keywords: WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM, WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM, WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM, WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM, WS_XML_CANONICALIZATION_ALGORITHM, WS_XML_CANONICALIZATION_ALGORITHM enumeration [Web Services for Windows], webservices/WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM, webservices/WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM, webservices/WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM, webservices/WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM, webservices/WS_XML_CANONICALIZATION_ALGORITHM, wsw.ws_xml_canonicalization_algorithm
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
req.typenames: WS_XML_CANONICALIZATION_ALGORITHM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_CANONICALIZATION_ALGORITHM
 - webservices/WS_XML_CANONICALIZATION_ALGORITHM
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
 - WS_XML_CANONICALIZATION_ALGORITHM
---

# WS_XML_CANONICALIZATION_ALGORITHM enumeration


## -description

The values for the XML canonicalization algorithms.

## -enum-fields

### -field WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM:0

The exclusive XML canonicalization algorithm
          represented by the URI 'http://www.w3.org/2001/10/xml-exc-c14n#' and
          defined in <a href="http://tools.ietf.org/html/rfc3741">RFC 3741</a>.

### -field WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM:1

The exclusive XML canonicalization with comments algorithm
          defined in <a href="http://tools.ietf.org/html/rfc3741">RFC 3741</a>.

### -field WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM:2

The inclusive XML canonicalization algorithm
          defined in <a href="https://www.w3.org/TR/xml-c14n">Canonical XML
Version 1.0</a>.
        

Inclusive canonicalization can only be applied to entire xml documents.

### -field WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM:3

The inclusive XML canonicalization with comments algorithm
          represented by the URI 'http://www.w3.org/TR/2001/REC-xml-c14n-20010315#WithComments' and
          defined in <a href="https://www.w3.org/TR/xml-c14n">Canonical XML
Version 1.0</a>.
        

Inclusive canonicalization can only be applied to entire xml documents.

