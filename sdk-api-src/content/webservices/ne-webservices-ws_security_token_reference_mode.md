---
UID: NE:webservices.__unnamed_enum_64
title: WS_SECURITY_TOKEN_REFERENCE_MODE (webservices.h)
description: With message and mixed-mode security bindings, the mechanism to use to refer to a security token from signatures, encrypted items and derived tokens.
helpviewer_keywords: ["WS_SECURITY_TOKEN_REFERENCE_MODE","WS_SECURITY_TOKEN_REFERENCE_MODE enumeration [Web Services for Windows]","WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT","WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID","WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID","WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID","WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID","webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER","wsw.ws_security_token_reference_mode"]
old-location: wsw\ws_security_token_reference_mode.htm
tech.root: wsw
ms.assetid: 09cd0350-d310-4335-9850-e0f6246be472
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_TOKEN_REFERENCE_MODE, WS_SECURITY_TOKEN_REFERENCE_MODE enumeration [Web Services for Windows], WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT, WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID, WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID, WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID, WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID, webservices/WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER, wsw.ws_security_token_reference_mode
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
req.typenames: WS_SECURITY_TOKEN_REFERENCE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_TOKEN_REFERENCE_MODE
 - webservices/WS_SECURITY_TOKEN_REFERENCE_MODE
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
 - WS_SECURITY_TOKEN_REFERENCE_MODE
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

### -field WS_SECURITY_TOKEN_REFERENCE_MODE_LOCAL_ID:1

The id of the serialized security token is used to refer to it.  This
reference mechanism can be used only when the security token is
serialized in the same message as the item (such as a signature) that
needs to refer to the security token.

### -field WS_SECURITY_TOKEN_REFERENCE_MODE_XML_BUFFER:2

An opaque XML buffer that is used as a token reference (for example, as in a custom token).

### -field WS_SECURITY_TOKEN_REFERENCE_MODE_CERT_THUMBPRINT:3

The thumbprint of a certificate is used to refer to it.

### -field WS_SECURITY_TOKEN_REFERENCE_MODE_SECURITY_CONTEXT_ID:4

The context-id is used to refer to a security context token.

### -field WS_SECURITY_TOKEN_REFERENCE_MODE_SAML_ASSERTION_ID:5

The SAML assertion ID is used to refer to the SAML token.

