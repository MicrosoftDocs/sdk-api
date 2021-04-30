---
UID: NS:webservices._WS_CERT_SIGNED_SAML_AUTHENTICATOR
title: WS_CERT_SIGNED_SAML_AUTHENTICATOR (webservices.h)
description: The type for specifying a SAML token authenticator based on an array of expected issuer certificates.
helpviewer_keywords: ["WS_CERT_SIGNED_SAML_AUTHENTICATOR","WS_CERT_SIGNED_SAML_AUTHENTICATOR structure [Web Services for Windows]","webservices/WS_CERT_SIGNED_SAML_AUTHENTICATOR","wsw.ws_cert_signed_saml_authenticator"]
old-location: wsw\ws_cert_signed_saml_authenticator.htm
tech.root: wsw
ms.assetid: 228ba94f-6e99-4bbf-93be-19d0311985ee
ms.date: 12/05/2018
ms.keywords: WS_CERT_SIGNED_SAML_AUTHENTICATOR, WS_CERT_SIGNED_SAML_AUTHENTICATOR structure [Web Services for Windows], webservices/WS_CERT_SIGNED_SAML_AUTHENTICATOR, wsw.ws_cert_signed_saml_authenticator
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
req.typenames: WS_CERT_SIGNED_SAML_AUTHENTICATOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CERT_SIGNED_SAML_AUTHENTICATOR
 - webservices/_WS_CERT_SIGNED_SAML_AUTHENTICATOR
 - WS_CERT_SIGNED_SAML_AUTHENTICATOR
 - webservices/WS_CERT_SIGNED_SAML_AUTHENTICATOR
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
 - WS_CERT_SIGNED_SAML_AUTHENTICATOR
---

# WS_CERT_SIGNED_SAML_AUTHENTICATOR structure


## -description

The type for specifying a SAML token authenticator based on an array
of expected issuer certificates.  When an authenticator of this type
is used, an incoming SAML token will be accepted if only if it has a
valid XML signature created with any one of the specified X.509
certificates.  Thus, the specified X.509 certificates represent a
'allow list' of trusted SAML issuers.
           

No revocation or chain trust checks are done by the runtime on the
specified certificates: so, it is up to the application to make sure
that the certificates are valid before they are specified in this
structure.
           

As indicated above, the validation of the received SAML is limited to
making sure that it was signed correctly by one of the specified
certificates.  The application may then extract the SAML assertion
using <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmessageproperty">WsGetMessageProperty</a> with the key 
<a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_SAML_ASSERTION</a> and do
additional validator or processing.

## -struct-fields

### -field authenticator

The base type from which this type and all other SAML authenticator
types derive.

### -field trustedIssuerCerts

The array of acceptable SAML issuers, identified by their X.509
certificates.  This field is required.
                

The certificate handles are duplicated and the copies are kept for
internal use.  The application continues to own the certificate
handles supplied here and is responsible for freeing them anytime
after the listener creation call that uses this structure returns.

### -field trustedIssuerCertCount

The count of X.509 certificates specified in trustedIssuerCerts.

### -field decryptionCert

The certificate for decrypting incoming SAML tokens.
                

The certificate handle is duplicated and the copy is kept for internal
use.  The application continues to own the certificate handle supplied
here and is responsible for freeing it anytime after the listener
creation call that uses this structure returns.

### -field _CERT_CONTEXT

### -field samlValidator

An optional callback to enable the application to additional
validation on the SAML assertion if the signature validation passes.

### -field samlValidatorCallbackState

The state to be passed back when invoking the samlValidator callback.