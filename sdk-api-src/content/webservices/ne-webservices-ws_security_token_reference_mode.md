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

# WS_SECURITY_TOKEN_REFERENCE_MODE enumeration


## -description



With message and mixed-mode security bindings, the mechanism to use to
refer to a security token from signatures, encrypted items and derived
tokens.  The security runtime can use the right reference on its own
most of the time, and this needs to be explicitly set only when a
specific reference mechanism is required, typically for interop with
another platform that supports only that reference form.
            


## -enum-fields




### -field WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID


The id of the serialized security token is used to refer to it.  This
reference mechanism can be used only when the security token is
serialized in the same message as the item (such as a signature) that
needs to refer to the security token.
                


### -field WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER


An opaque XML buffer that is used as a token reference (for example, as in a custom token).


### -field WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT


The thumbprint of a certificate is used to refer to it.
                


### -field WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID


              The context-id is used to refer to a security context token.
            


### -field WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID


              The SAML assertion ID is used to refer to the SAML token.
            

