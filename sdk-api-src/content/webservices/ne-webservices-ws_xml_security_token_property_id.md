---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

