---
UID: NE:webservices.__unnamed_enum_63
title: WS_SECURITY_ALGORITHM_SUITE_NAME (webservices.h)
description: A suite of security algorithms used for tasks such as signing and encrypting. The values in this enumeration correspond to the suites defined in WS-SecurityPolicy 1.1section 7.1.
helpviewer_keywords: ["WS_SECURITY_ALGORITHM_SUITE_NAME","WS_SECURITY_ALGORITHM_SUITE_NAME enumeration [Web Services for Windows]","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256","WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256","webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15","wsw.ws_security_algorithm_suite_name"]
old-location: wsw\ws_security_algorithm_suite_name.htm
tech.root: wsw
ms.assetid: cd7116d2-86f6-475e-a55d-050c7e02172d
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_ALGORITHM_SUITE_NAME, WS_SECURITY_ALGORITHM_SUITE_NAME enumeration [Web Services for Windows], WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15, wsw.ws_security_algorithm_suite_name
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
req.typenames: WS_SECURITY_ALGORITHM_SUITE_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_ALGORITHM_SUITE_NAME
 - webservices/WS_SECURITY_ALGORITHM_SUITE_NAME
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
 - WS_SECURITY_ALGORITHM_SUITE_NAME
---

# WS_SECURITY_ALGORITHM_SUITE_NAME enumeration


## -description

A suite of security algorithms used for tasks such as signing and encrypting. 
        The values in this enumeration correspond to the suites defined in 
        WS-SecurityPolicy 1.1section 7.1.

## -enum-fields

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256:1

Identifies the Basic256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192:2

Identifies the Basic192 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128:3

Identifies the Basic128 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15:4

Identifies the Basic256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15:5

Identifies the Basic192Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15:6

Identifies the Basic128RSA15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256:7

Identifies the Basic256Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256:8

Identifies the Basic192Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256:9

Identifies the Basic128Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15:10

Identifies the Basic256Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15:11

Identifies the Basic192Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.

### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15:12

Identifies the Basic128Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_id">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
