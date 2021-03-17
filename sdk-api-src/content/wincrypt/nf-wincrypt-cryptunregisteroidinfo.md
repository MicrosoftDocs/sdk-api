---
UID: NF:wincrypt.CryptUnregisterOIDInfo
title: CryptUnregisterOIDInfo function (wincrypt.h)
description: The CryptUnregisterOIDInfo function removes the registration of a specified CRYPT_OID_INFO OID information structure. The structure to be unregistered is identified by the structure's pszOID and dwGroupId members.
helpviewer_keywords: ["CryptUnregisterOIDInfo","CryptUnregisterOIDInfo function [Security]","_crypto2_cryptunregisteroidinfo","security.cryptunregisteroidinfo","wincrypt/CryptUnregisterOIDInfo"]
old-location: security\cryptunregisteroidinfo.htm
tech.root: security
ms.assetid: 1217397b-2af9-4f58-8616-5a18ee2f4b8c
ms.date: 12/05/2018
ms.keywords: CryptUnregisterOIDInfo, CryptUnregisterOIDInfo function [Security], _crypto2_cryptunregisteroidinfo, security.cryptunregisteroidinfo, wincrypt/CryptUnregisterOIDInfo
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
 - CryptUnregisterOIDInfo
 - wincrypt/CryptUnregisterOIDInfo
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
 - CryptUnregisterOIDInfo
---

# CryptUnregisterOIDInfo function


## -description

The <b>CryptUnregisterOIDInfo</b> function removes the registration of a specified 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> OID information structure. The structure to be unregistered is identified by the structure's <b>pszOID</b> and <b>dwGroupId</b> members.

## -parameters

### -param pInfo [in]

Specifies the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) information for which the registration is to be removed. The group that the registration is removed for is specified by the <b>dwGroupId</b> member in the <i>pInfo</i>.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidinfo">CryptRegisterOIDInfo</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>