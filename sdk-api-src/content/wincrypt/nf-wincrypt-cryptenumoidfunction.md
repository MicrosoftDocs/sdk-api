---
UID: NF:wincrypt.CryptEnumOIDFunction
title: CryptEnumOIDFunction function (wincrypt.h)
description: The CryptEnumOIDFunction function enumerates the registered object identifier (OID) functions.
helpviewer_keywords: ["CryptEnumOIDFunction","CryptEnumOIDFunction function [Security]","_crypto2_cryptenumoidfunction","security.cryptenumoidfunction","wincrypt/CryptEnumOIDFunction"]
old-location: security\cryptenumoidfunction.htm
tech.root: security
ms.assetid: aa2fba03-183b-4b74-b306-8f4592995897
ms.date: 12/05/2018
ms.keywords: CryptEnumOIDFunction, CryptEnumOIDFunction function [Security], _crypto2_cryptenumoidfunction, security.cryptenumoidfunction, wincrypt/CryptEnumOIDFunction
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptEnumOIDFunction
 - wincrypt/CryptEnumOIDFunction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptEnumOIDFunction
---

# CryptEnumOIDFunction function


## -description

The <b>CryptEnumOIDFunction</b> function enumerates the registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) functions. OID functions that are enumerated can be screened to include those identified by their encoding type, function name, OID, or any combination of encoding type, function name, and OID. For each OID function that matches the selection criteria, an application-provided callback function, <b>pfnEnumOIDFunc</b>, is called.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type to match. Setting this parameter to CRYPT_MATCH_ANY_ENCODING_TYPE matches any encoding type. Note that if CRYPT_MATCH_ANY_ENCODING_TYPE is not specified, either a certificate or <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> is required. If the low-order word that contains the certificate encoding type is nonzero, it is used; otherwise, the high-order word that contains the message encoding type is used. If both are specified, the certificate encoding type in the low-order word is used. 




Currently defined encoding types are:

<ul>
<li>CRYPT_ASN_ENCODING</li>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
<li>CRYPT_MATCH_ANY_ENCODING_TYPE</li>
</ul>

### -param pszFuncName [in]

Name of a function for which a case insensitive match search is performed. Setting this parameter to <b>NULL</b> results in a match being found for any function name.

### -param pszOID [in]

If the high-order word of <i>pszOID</i> is nonzero, <i>pszOID</i> specifies the object identifier for which a case insensitive match search is performed. If the high-order word of <i>pszOID</i> is zero, <i>pszOID</i> is used to match a numeric object identifier. Setting this parameter to <b>NULL</b> matches any object identifier. Setting this parameter to CRYPT_DEFAULT_OID restricts the enumeration to only the default functions.

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param pvArg [in]

A pointer to arguments to be passed through to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func">CRYPT_ENUM_OID_FUNCTION</a> callback function.

### -param pfnEnumOIDFunc [in]

A pointer to the callback function that is executed for each OID function that matches the input parameters. For details, see <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func">CRYPT_ENUM_OID_FUNCTION</a>.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>