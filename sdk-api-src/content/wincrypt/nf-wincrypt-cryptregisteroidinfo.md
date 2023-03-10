---
UID: NF:wincrypt.CryptRegisterOIDInfo
title: CryptRegisterOIDInfo function (wincrypt.h)
description: The CryptRegisterOIDInfo function registers the OID information specified in the CRYPT_OID_INFO structure, persisting it to the registry.
helpviewer_keywords: ["CryptRegisterOIDInfo","CryptRegisterOIDInfo function [Security]","_crypto2_cryptregisteroidinfo","security.cryptregisteroidinfo","wincrypt/CryptRegisterOIDInfo"]
old-location: security\cryptregisteroidinfo.htm
tech.root: security
ms.assetid: 7a5b4800-3182-4cd4-b17a-c6d4e11f7047
ms.date: 12/05/2018
ms.keywords: CryptRegisterOIDInfo, CryptRegisterOIDInfo function [Security], _crypto2_cryptregisteroidinfo, security.cryptregisteroidinfo, wincrypt/CryptRegisterOIDInfo
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
 - CryptRegisterOIDInfo
 - wincrypt/CryptRegisterOIDInfo
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
 - CryptRegisterOIDInfo
---

# CryptRegisterOIDInfo function


## -description

The <b>CryptRegisterOIDInfo</b> function registers the OID information specified in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure, persisting it to the registry.

Crypt32.dll contains predefined information for the commonly known OIDs. This function allows applications to augment the predefined OID information. During 
<b>CryptRegisterOIDInfo</b>'s first call, the registered OID information is installed.

When expanding the tables using <b>CryptRegisterOIDInfo</b>, the new entries can be placed either before or after predefined entries, controlled by <i>dwFlags</i>. The placement of registered OID information affects the result of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> because the tables are searched in order. First registered entries placed before the predefined entries are checked, then the predefined entries are checked, and finally, registered entries placed after the predefined entries are checked. The first match found is returned. A newly registered entry placed before the predefined entries can override one of the predefined entries.

## -parameters

### -param pInfo [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure with the OID information to register. Specify the group that the OID information is to be registered for by setting the <b>dwGroupId</b> member of the structure.

<div class="alert"><b>Note</b>  <p class="note">When registering OID information for <a href="/windows/desktop/SecGloss/s-gly">Suite B</a> algorithms implemented with <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a> (CNG), you must set the <b>Algid</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure to <b>CALG_OID_INFO_CNG_ONLY</b> (0xFFFFFFFF).

</div>
<div> </div>

### -param dwFlags [in]

By default, the registered OID information is installed after Crypt32.dll's OID entries. If CRYPT_INSTALL_OID_INFO_BEFORE_FLAG is set, new OID information is install before Crypt32.dll's entries.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

## -remarks

When you have finished using the OID information, unregister it by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptunregisteroidinfo">CryptUnregisterOIDInfo</a>  function.

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumoidinfo">CryptEnumOIDInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptunregisteroidinfo">CryptUnregisterOIDInfo</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>