---
UID: NE:webservices.__unnamed_enum_77
title: WS_XML_SECURITY_TOKEN_PROPERTY_ID (webservices.h)
description: The keys for the bag of properties for the creation of XML security tokens. This enumeration is used within the WS_XML_SECURITY_TOKEN_PROPERTY structure, which is used as parameter for WsCreateXmlSecurityToken.
helpviewer_keywords: ["WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE","WS_XML_SECURITY_TOKEN_PROPERTY_ID","WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows]","WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE","WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME","WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME","webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE","webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ID","webservices/WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE","webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME","webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME","wsw.ws_xml_security_token_property_id"]
old-location: wsw\ws_xml_security_token_property_id.htm
tech.root: wsw
ms.assetid: 78133ccf-4e3c-4c1b-97af-1a487b444ee0
ms.date: 12/05/2018
ms.keywords: WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE, WS_XML_SECURITY_TOKEN_PROPERTY_ID, WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE, WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ID, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, wsw.ws_xml_security_token_property_id
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
req.typenames: WS_XML_SECURITY_TOKEN_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_SECURITY_TOKEN_PROPERTY_ID
 - webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ID
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
 - WS_XML_SECURITY_TOKEN_PROPERTY_ID
---

# WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration


## -description

The keys for the bag of properties for the creation of XML security tokens. This enumeration is used within the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_security_token_property">WS_XML_SECURITY_TOKEN_PROPERTY</a> structure, which is used as parameter for <a href="/windows/desktop/api/webservices/nf-webservices-wscreatexmlsecuritytoken">WsCreateXmlSecurityToken</a>.

## -enum-fields

### -field WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE:1

A pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> that contains
the XML form of the reference to be used for this token (from a
signature, for example) when the token is attached to (for example, serialized
in) a message.  This is required if and only if the token is a
proof-of-possession token.  If specified, the XML buffer must have
exactly one top level XML element.

### -field WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE:2

A pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> that contains the XML form of the reference to be used for this token (from a
signature, for example) when the token is not attached to a message.  This
should be specified only if the token is a proof-of-possession token,
and is used without being serialized in the message.  If specified,
the XML buffer must have exactly one top level XML element.

### -field WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME:3

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> structure that contains the time from when the security token is valid.

### -field WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME:4

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> structure that contains the time until when the security token is valid.
