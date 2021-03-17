---
UID: NF:wincrypt.CryptUnregisterOIDFunction
title: CryptUnregisterOIDFunction function (wincrypt.h)
description: Removes the registration of a DLL that contains the function to be called for the specified encoding type, function name, and OID.
helpviewer_keywords: ["CryptUnregisterOIDFunction","CryptUnregisterOIDFunction function [Security]","_crypto2_cryptunregisteroidfunction","security.cryptunregisteroidfunction","wincrypt/CryptUnregisterOIDFunction"]
old-location: security\cryptunregisteroidfunction.htm
tech.root: security
ms.assetid: c06ffda5-df7c-4e0e-bf4f-8b8c968fcd4c
ms.date: 12/05/2018
ms.keywords: CryptUnregisterOIDFunction, CryptUnregisterOIDFunction function [Security], _crypto2_cryptunregisteroidfunction, security.cryptunregisteroidfunction, wincrypt/CryptUnregisterOIDFunction
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CryptUnregisterOIDFunction
 - wincrypt/CryptUnregisterOIDFunction
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
 - CryptUnregisterOIDFunction
---

# CryptUnregisterOIDFunction function


## -description

The <b>CryptUnregisterOIDFunction</b> function removes the registration of a DLL that contains the function to be called for the specified encoding type, function name, and OID.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are used; however, additional encoding types may be added in the future. To match both current encoding types, use: 



X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

For functions that do not use an encoding type, set this parameter to zero.

### -param pszFuncName [in]

Name of the function being unregistered.

### -param pszOID [in]

A pointer to the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that corresponds to the name of the function being unregistered. If the high order word of the OID is nonzero, <i>pszOID</i> is a pointer to either an OID string such as "2.5.29.1" or an <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> string such as "file." If the high order word of the OID is zero, the low order word specifies the integer identifier to be used as the object identifier.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>