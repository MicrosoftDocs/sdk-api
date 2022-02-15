---
UID: NE:webservices.__unnamed_enum_2
title: WS_XML_CANONICALIZATION_PROPERTY_ID (webservices.h)
description: Identifies each XML canonicalization property and its associated value. This enumeration is used within the WS_XML_CANONICALIZATION_PROPERTY structure, which is used as a parameter to WsStartReaderCanonicalization and WsStartWriterCanonicalization.
helpviewer_keywords: ["WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM","WS_XML_CANONICALIZATION_PROPERTY_ID","WS_XML_CANONICALIZATION_PROPERTY_ID enumeration [Web Services for Windows]","WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES","WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT","WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE","webservices/WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM","webservices/WS_XML_CANONICALIZATION_PROPERTY_ID","webservices/WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES","webservices/WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT","webservices/WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE","wsw.ws_xml_canonicalization_property_id"]
old-location: wsw\ws_xml_canonicalization_property_id.htm
tech.root: wsw
ms.assetid: af96e1e7-d7e8-4e38-a8ae-f8f28cf0eda9
ms.date: 12/05/2018
ms.keywords: WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM, WS_XML_CANONICALIZATION_PROPERTY_ID, WS_XML_CANONICALIZATION_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES, WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT, WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE, webservices/WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM, webservices/WS_XML_CANONICALIZATION_PROPERTY_ID, webservices/WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES, webservices/WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT, webservices/WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE, wsw.ws_xml_canonicalization_property_id
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_XML_CANONICALIZATION_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_CANONICALIZATION_PROPERTY_ID
 - webservices/WS_XML_CANONICALIZATION_PROPERTY_ID
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
 - WS_XML_CANONICALIZATION_PROPERTY_ID
---

# WS_XML_CANONICALIZATION_PROPERTY_ID enumeration


## -description

Identifies each XML canonicalization property and its associated
        value.  This enumeration is used within the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_canonicalization_property">WS_XML_CANONICALIZATION_PROPERTY</a> structure, which is used as a parameter to <a href="/windows/desktop/api/webservices/nf-webservices-wsstartreadercanonicalization">WsStartReaderCanonicalization</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsstartwritercanonicalization">WsStartWriterCanonicalization</a>.

## -enum-fields

### -field WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM:0

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_canonicalization_algorithm">WS_XML_CANONICALIZATION_ALGORITHM</a> value that specifies the algorithm to be used for canonicalization.  If this is not specified,
          the <b>WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM</b> is used.

### -field WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES:1

A <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes">WS_XML_CANONICALIZATION_INCLUSIVE_PREFIXES</a> structure that contains the set of prefixes to be treated as inclusive prefixes when using
          the exclusive canonicalization algorithm.  If this is not specified,
          no prefix is treated as an inclusive prefix.

### -field WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT:2

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_qname">WS_XML_QNAME</a> structure that contains the elements to be omitted during canonicalization.  If one or more
          elements in the XML input match the specified name and namespace, then
          all such elements and the subtrees rooted at them are omitted from the
          canonical output.  This property can be used to implement enveloped
          signatures where canonicalization needs to skip a signature element
          that is embedded within the XML content being canonicalized and
          signed.  If this is not specified, no element is omitted from the
          output.

### -field WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE:3

A <b>ULONG</b> that specifies the size of the buffer in which canonical bytes are accumulated.  Once at least this
          many bytes are generated, or canonicalization is ended by a call to <a href="/windows/desktop/api/webservices/nf-webservices-wsendreadercanonicalization">WsEndReaderCanonicalization</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a>, the canonical bytes are
          written to the output specified at the start of canonicalization.  If this is
          not specified, a default buffer size of 1024 is used.
