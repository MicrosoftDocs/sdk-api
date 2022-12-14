---
UID: NS:sspi._SecPkgContext_NegotiatedTlsExtensions
title: SecPkgContext_NegotiatedTlsExtensions
ms.date: 11/4/2019
targetos: Windows
description: The SecPkgContext_NegotiatedTlsExtensions structure contains information about the (D)TLS extensions negotiated for the current (D)TLS connection.
tech.root: security
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.target-type: Windows
req.typenames: SecPkgContext_NegotiatedTlsExtensions, *PSecPkgContext_NegotiatedTlsExtensions
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SecPkgContext_NegotiatedTlsExtensions
 - SecPkgContext_NegotiatedTlsExtensions
f1_keywords:
 - _SecPkgContext_NegotiatedTlsExtensions
 - sspi/_SecPkgContext_NegotiatedTlsExtensions
 - PSecPkgContext_NegotiatedTlsExtensions
 - sspi/PSecPkgContext_NegotiatedTlsExtensions
 - SecPkgContext_NegotiatedTlsExtensions
 - sspi/SecPkgContext_NegotiatedTlsExtensions
dev_langs:
 - c++
---

## -description

The **SecPkgContext_NegotiatedTlsExtensions** structure contains information about the (D)TLS extensions negotiated for the current (D)TLS connection.

## -struct-fields

### -field ExtensionsCount

The number of negotiated (D)TLS extensions.

### -field Extensions

A pointer to the array of 2-byte TLS extension IDs as defined in the [IANA (D)TLS extensions registry](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml).

## -remarks

The list of (D)TLS extensions returned via this structure is not exhaustive. Depending on the type of the (D)TLS extension, it is not always possible to determine whether it has been negotiated with the peer. This structure generally reports negotiable (D)TLS extensions of interest to SSPI callers, such as: Certificate Status Request, Application Layer Protocol Negotiation, Secure Real-time Transport Protocol, Token Binding, Extended Master Secret, Renegotiation Info.

## -see-also

[IANA (D)TLS extensions registry](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml)

[QueryContextAttributes (Schannel) function](/windows/win32/secauthn/querycontextattributes--schannel)

