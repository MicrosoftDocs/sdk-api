---
UID: NS:webservices._WS_SECURITY_ALGORITHM_SUITE
title: WS_SECURITY_ALGORITHM_SUITE (webservices.h)
description: Defines the security algorithms and key lengths to be used with WS-Security. This setting is relevant to message security bindings and mixed-mode security bindings.
helpviewer_keywords: ["WS_SECURITY_ALGORITHM_SUITE","WS_SECURITY_ALGORITHM_SUITE structure [Web Services for Windows]","webservices/WS_SECURITY_ALGORITHM_SUITE","wsw.ws_security_algorithm_suite"]
old-location: wsw\ws_security_algorithm_suite.htm
tech.root: wsw
ms.assetid: aa2bb951-47ba-4241-b29a-2f54b92da4cb
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_ALGORITHM_SUITE, WS_SECURITY_ALGORITHM_SUITE structure [Web Services for Windows], webservices/WS_SECURITY_ALGORITHM_SUITE, wsw.ws_security_algorithm_suite
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
req.typenames: WS_SECURITY_ALGORITHM_SUITE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_ALGORITHM_SUITE
 - webservices/_WS_SECURITY_ALGORITHM_SUITE
 - WS_SECURITY_ALGORITHM_SUITE
 - webservices/WS_SECURITY_ALGORITHM_SUITE
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
 - WS_SECURITY_ALGORITHM_SUITE
---

# WS_SECURITY_ALGORITHM_SUITE structure


## -description

Defines the security algorithms and key lengths to be used with
WS-Security.  This setting is relevant to message security bindings
and mixed-mode security bindings.

## -struct-fields

### -field canonicalizationAlgorithm

Algorithm to use for XML canonicalization, such as the exclusive XML
canonicalization algorithm. 
Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to 
<b>WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</b>.

### -field digestAlgorithm

Algorithm to use for message part digests, such as SHA-1, SHA-256,
SHA-384, or SHA-512. 
Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to 
<b>WS_SECURITY_ALGORITHM_DIGEST_SHA1</b>.

### -field symmetricSignatureAlgorithm

Algorithm to use for message authentication codes (also known as MACs
or symmetric signatures) such as HMAC-SHA1, HMAC-SHA256, HMAC-SHA384, or HMAC-SHA512. 
Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to 
<b>WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</b>.

### -field asymmetricSignatureAlgorithm

Algorithm to use for asymmetric signatures. 
Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to 
<b>WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</b>.

### -field encryptionAlgorithm

Algorithm to use for message part encryption. Reserved for future use. Should be set to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a>.

### -field keyDerivationAlgorithm

Algorithm to use for deriving keys from other symmetric keys. 
Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to 
<b>WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</b>.

### -field symmetricKeyWrapAlgorithm

Algorithm to use for encrypting symmetric keys with other symmetric
keys. Reserved for future use. Should be set to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a>.

### -field asymmetricKeyWrapAlgorithm

Algorithm to use for encrypting symmetric keys with asymmetric
                  keys. Setting this value to <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DEFAULT</a> will default to
                  <b>WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</b>.

### -field minSymmetricKeyLength

The minimum key length (in bits) of symmetric key security tokens. 
Setting this value to 0 will default to 128 bits.

### -field maxSymmetricKeyLength

The maximum key length (in bits) of symmetric key security tokens. 
Setting this value to 0 will default to 512 bits.

### -field minAsymmetricKeyLength

The minimum key length (in bits) of asymmetric key security tokens.
Setting this value to 0 will default to 1024 bits.

### -field maxAsymmetricKeyLength

The maximum key length (in bits) of asymmetric key security tokens.
Setting this value to 0 will default to 16384 bits.

### -field properties

Algorithm properties. Reserved for future use. Should be set to <b>NULL</b>.

### -field propertyCount

Number of entries in properties array. Reserved for future use. Should be set to 0.

## -remarks

When key derivation is used, the key length restrictions apply to the
source security token from which the signing or encryption derived
token are derived.