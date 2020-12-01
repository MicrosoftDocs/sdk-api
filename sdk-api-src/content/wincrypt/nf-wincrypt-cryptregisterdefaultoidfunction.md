---
UID: NF:wincrypt.CryptRegisterDefaultOIDFunction
title: CryptRegisterDefaultOIDFunction function (wincrypt.h)
description: The CryptRegisterDefaultOIDFunction registers a DLL containing the default function to be called for the specified encoding type and function name. Unlike CryptRegisterOIDFunction, the function name to be exported by the DLL cannot be overridden.
helpviewer_keywords: ["CryptRegisterDefaultOIDFunction","CryptRegisterDefaultOIDFunction function [Security]","_crypto2_cryptregisterdefaultoidfunction","security.cryptregisterdefaultoidfunction","wincrypt/CryptRegisterDefaultOIDFunction"]
old-location: security\cryptregisterdefaultoidfunction.htm
tech.root: security
ms.assetid: 9633cce4-538e-490e-8a5a-6b28f161a09d
ms.date: 12/05/2018
ms.keywords: CryptRegisterDefaultOIDFunction, CryptRegisterDefaultOIDFunction function [Security], _crypto2_cryptregisterdefaultoidfunction, security.cryptregisterdefaultoidfunction, wincrypt/CryptRegisterDefaultOIDFunction
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
 - CryptRegisterDefaultOIDFunction
 - wincrypt/CryptRegisterDefaultOIDFunction
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
 - CryptRegisterDefaultOIDFunction
---

# CryptRegisterDefaultOIDFunction function


## -description

The <b>CryptRegisterDefaultOIDFunction</b> registers a DLL containing the default function to be called for the specified encoding type and function name. Unlike 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidfunction">CryptRegisterOIDFunction</a>, the function name to be exported by the DLL cannot be overridden.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param pszFuncName [in]

Name of the function being registered.

### -param dwIndex [in]

Index location for the insertion of the DLL in the list of DLLs. If <i>dwIndex</i> is zero, the DLL is inserted at the beginning of the list. If it is CRYPT_REGISTER_LAST_INDEX, the DLL is appended at the end of the list.

### -param pwszDll [in]

Optional environment-variable string to be expanded using <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">ExpandEnvironmentStrings</a> function before loading the DLL.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>