---
UID: NF:wincrypt.CertAlgIdToOID
title: CertAlgIdToOID function (wincrypt.h)
description: Converts a CryptoAPI algorithm identifier (ALG_ID) to an Abstract Syntax Notation One (ASN.1) object identifier (OID) string.
helpviewer_keywords: ["CertAlgIdToOID","CertAlgIdToOID function [Security]","_crypto2_certalgidtooid","security.certalgidtooid","wincrypt/CertAlgIdToOID"]
old-location: security\certalgidtooid.htm
tech.root: security
ms.assetid: 2a66c6da-22dd-4192-9f3d-2fb85f8032e0
ms.date: 12/05/2018
ms.keywords: CertAlgIdToOID, CertAlgIdToOID function [Security], _crypto2_certalgidtooid, security.certalgidtooid, wincrypt/CertAlgIdToOID
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
 - CertAlgIdToOID
 - wincrypt/CertAlgIdToOID
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
 - CertAlgIdToOID
---

# CertAlgIdToOID function


## -description

Use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function instead of this function because <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> identifiers are no longer supported in CNG. Use the <b>CRYPT_OID_INFO_CNG_ALGID_KEY</b> value in the <i>dwKeyType</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function instead.

<b>Windows Server 2003 and Windows XP:  </b>The <b>CertAlgIdToOID</b> function converts a <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a> algorithm identifier (<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>) to an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string.

## -parameters

### -param dwAlgId [in]

Value to be converted to an OID.

## -returns

If the function succeeds, the function returns the null-terminated OID string.

If no OID string corresponds to the algorithm identifier, the function returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Conversion Functions</a>