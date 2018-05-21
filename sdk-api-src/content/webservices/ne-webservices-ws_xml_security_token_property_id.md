---
UID: NE:webservices.WS_XML_SECURITY_TOKEN_PROPERTY_ID
title: WS_XML_SECURITY_TOKEN_PROPERTY_ID
author: windows-driver-content
description: The keys for the bag of properties for the creation of XML security tokens. This enumeration is used within the WS_XML_SECURITY_TOKEN_PROPERTY structure, which is used as parameter for WsCreateXmlSecurityToken.
old-location: wsw\ws_xml_security_token_property_id.htm
old-project: wsw
ms.assetid: 78133ccf-4e3c-4c1b-97af-1a487b444ee0
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE, WS_XML_SECURITY_TOKEN_PROPERTY_ID, WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE, WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_ID, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, webservices/WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, wsw.ws_xml_security_token_property_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_XML_SECURITY_TOKEN_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_SECURITY_TOKEN_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration


## -description


The keys for the bag of properties for the creation of XML security tokens. This enumeration is used within the <a href="https://msdn.microsoft.com/dd235e33-39f7-459d-8b7f-76d5c3f96770">WS_XML_SECURITY_TOKEN_PROPERTY</a> structure, which is used as parameter for <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">WsCreateXmlSecurityToken</a>.
            


## -enum-fields




### -field WS_XML_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE

A pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that contains
the XML form of the reference to be used for this token (from a
signature, for example) when the token is attached to (for example, serialized
in) a message.  This is required if and only if the token is a
proof-of-possession token.  If specified, the XML buffer must have
exactly one top level XML element.
                


### -field WS_XML_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE


A pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that contains the XML form of the reference to be used for this token (from a
signature, for example) when the token is not attached to a message.  This
should be specified only if the token is a proof-of-possession token,
and is used without being serialized in the message.  If specified,
the XML buffer must have exactly one top level XML element.
                


### -field WS_XML_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME


A <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> structure that contains the time from when the security token is valid.


### -field WS_XML_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME


A <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> structure that contains the time until when the security token is valid.

