---
UID: NF:wincrypt.CertOIDToAlgId
title: CertOIDToAlgId function (wincrypt.h)
description: Use the CryptFindOIDInfo function instead of this function because ALG_ID identifiers are no longer supported in CNG.
helpviewer_keywords: ["CertOIDToAlgId","CertOIDToAlgId function [Security]","_crypto2_certoidtoalgid","security.certoidtoalgid","wincrypt/CertOIDToAlgId"]
old-location: security\certoidtoalgid.htm
tech.root: security
ms.assetid: 920b2642-ce7c-4098-8720-5a6f24128787
ms.date: 12/05/2018
ms.keywords: CertOIDToAlgId, CertOIDToAlgId function [Security], _crypto2_certoidtoalgid, security.certoidtoalgid, wincrypt/CertOIDToAlgId
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
 - CertOIDToAlgId
 - wincrypt/CertOIDToAlgId
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
 - CertOIDToAlgId
---

# CertOIDToAlgId function


## -description

Use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function instead of this function because <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> identifiers are no longer supported in CNG. Use the <b>CRYPT_OID_INFO_OID_KEY</b> value in the <i>dwKeyType</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function instead.

<b>Windows Server 2003 and Windows XP:  </b>The <b>CertOIDToAlgId</b> function converts the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string to the CryptoAPI algorithm identifier (<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>).

## -parameters

### -param pszObjId [in]

Pointer to the ASN.1 OID to be converted to an algorithm identifier.

## -returns

Returns the 
<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> that corresponds to the object identifier (OID) or zero if no <b>ALG_ID</b> corresponds to the OID.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Conversion Functions</a>