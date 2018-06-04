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

# _WS_CERT_SIGNED_SAML_AUTHENTICATOR structure


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
using <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> with the key 
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_SAML_ASSERTION</a> and do
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
                

