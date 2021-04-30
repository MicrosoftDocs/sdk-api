---
UID: NC:webservices.WS_VALIDATE_SAML_CALLBACK
title: WS_VALIDATE_SAML_CALLBACK (webservices.h)
description: Validates a SAML assertion.
helpviewer_keywords: ["WS_VALIDATE_SAML_CALLBACK","WS_VALIDATE_SAML_CALLBACK callback","WS_VALIDATE_SAML_CALLBACK callback function [Web Services for Windows]","webservices/WS_VALIDATE_SAML_CALLBACK","wsw.ws_validate_saml_callback"]
old-location: wsw\ws_validate_saml_callback.htm
tech.root: wsw
ms.assetid: 72cc10ae-ba0e-4f3a-a376-c0b1999b074e
ms.date: 12/05/2018
ms.keywords: WS_VALIDATE_SAML_CALLBACK, WS_VALIDATE_SAML_CALLBACK callback, WS_VALIDATE_SAML_CALLBACK callback function [Web Services for Windows], webservices/WS_VALIDATE_SAML_CALLBACK, wsw.ws_validate_saml_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_VALIDATE_SAML_CALLBACK
 - webservices/WS_VALIDATE_SAML_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_VALIDATE_SAML_CALLBACK
---

# WS_VALIDATE_SAML_CALLBACK callback function


## -description

Validates a SAML assertion.  If a
received SAML assertion passes the signature verification checks that
ensure the SAML was issued by a trusted issuer, then this callback is
invoked to enable the application to do additional validation on the
XML form of the SAML assertion.  This callback is expected to return
S_OK if the SAML assertion was successfully validated, S_FALSE when
the assertion could not be validated and an error value if an
unexpected error occurred.  Returning any result other than S_OK from
this callback will result in the associated receive message failing
with a security error.
            

As with all security callbacks, the application should expect to
receive this callback any time between listener open and close, but it
will never be invoked when a listener is not open.

## -parameters

### -param samlValidatorCallbackState [in, optional]

The state to be passed back when invoking this callback.

### -param samlAssertion [in]

The received SAML assertion that has undergone a successful signature check.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

