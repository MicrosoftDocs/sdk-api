---
UID: NS:sspi._SecPkgContext_KeyInfoW
title: SecPkgContext_KeyInfoW (sspi.h)
description: The SecPkgContext_KeyInfo structure contains information about the session keys used in a security context. (Unicode)
helpviewer_keywords: ["*PSecPkgContext_KeyInfoW","PSecPkgContext_KeyInfo","PSecPkgContext_KeyInfo structure pointer [Security]","SecPkgContext_KeyInfo","SecPkgContext_KeyInfo structure [Security]","SecPkgContext_KeyInfoA","SecPkgContext_KeyInfoW","_ssp_secpkgcontext_keyinfo","security.secpkgcontext_keyinfo","sspi/PSecPkgContext_KeyInfo","sspi/SecPkgContext_KeyInfo","sspi/SecPkgContext_KeyInfoA","sspi/SecPkgContext_KeyInfoW"]
old-location: security\secpkgcontext_keyinfo.htm
tech.root: security
ms.assetid: ec146329-6789-460c-ae62-629a1765a4c1
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_KeyInfoW, PSecPkgContext_KeyInfo, PSecPkgContext_KeyInfo structure pointer [Security], SecPkgContext_KeyInfo, SecPkgContext_KeyInfo structure [Security], SecPkgContext_KeyInfoA, SecPkgContext_KeyInfoW, _ssp_secpkgcontext_keyinfo, security.secpkgcontext_keyinfo, sspi/PSecPkgContext_KeyInfo, sspi/SecPkgContext_KeyInfo, sspi/SecPkgContext_KeyInfoA, sspi/SecPkgContext_KeyInfoW'
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_KeyInfoW (Unicode) and SecPkgContext_KeyInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_KeyInfoW, *PSecPkgContext_KeyInfoW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_KeyInfoW
 - sspi/_SecPkgContext_KeyInfoW
 - PSecPkgContext_KeyInfoW
 - sspi/PSecPkgContext_KeyInfoW
 - SecPkgContext_KeyInfoW
 - sspi/SecPkgContext_KeyInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_KeyInfo
 - SecPkgContext_KeyInfoA
 - SecPkgContext_KeyInfoW
---

# SecPkgContext_KeyInfoW structure


## -description

The <b>SecPkgContext_KeyInfo</b> structure contains information about the <a href="/windows/desktop/SecGloss/s-gly">session keys</a> used in a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

Applications using the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP) should not use the <b>SecPkgContext_KeyInfo</b> structure. Instead, use the <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo">SecPkgContext_ConnectionInfo</a> structure.

## -struct-fields

### -field sSignatureAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for generating signatures, for example "MD5" or "SHA-2".

### -field sEncryptAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for encrypting messages. Reserved for future use.

### -field KeySize

Specifies the effective key length, in bits, for the session key. This is typically 40, 56, or 128 bits.

### -field SignatureAlgorithm

Specifies the algorithm identifier (<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>) used for generating signatures, if available.

### -field EncryptAlgorithm

Specifies the algorithm identifier (<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>) used for encrypting messages. Reserved for future use.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgContext_KeyInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
