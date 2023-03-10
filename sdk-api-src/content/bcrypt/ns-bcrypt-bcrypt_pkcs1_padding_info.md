---
UID: NS:bcrypt._BCRYPT_PKCS1_PADDING_INFO
title: BCRYPT_PKCS1_PADDING_INFO (bcrypt.h)
description: Used to provide options for the PKCS
helpviewer_keywords: ["BCRYPT_PKCS1_PADDING_INFO","BCRYPT_PKCS1_PADDING_INFO structure [Security]","bcrypt/BCRYPT_PKCS1_PADDING_INFO","security.bcrypt_pkcs1_padding_info"]
old-location: security\bcrypt_pkcs1_padding_info.htm
tech.root: security
ms.assetid: 920fa461-5b7e-4429-972d-e7c83fb62c64
ms.date: 12/05/2018
ms.keywords: BCRYPT_PKCS1_PADDING_INFO, BCRYPT_PKCS1_PADDING_INFO structure [Security], bcrypt/BCRYPT_PKCS1_PADDING_INFO, security.bcrypt_pkcs1_padding_info
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BCRYPT_PKCS1_PADDING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_PKCS1_PADDING_INFO
 - bcrypt/_BCRYPT_PKCS1_PADDING_INFO
 - BCRYPT_PKCS1_PADDING_INFO
 - bcrypt/BCRYPT_PKCS1_PADDING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_PKCS1_PADDING_INFO
---

# BCRYPT_PKCS1_PADDING_INFO structure


## -description

The <b>BCRYPT_PKCS1_PADDING_INFO</b> structure is used to provide options for the <a href="/windows/desktop/SecGloss/p-gly">PKCS #1</a> padding scheme.

## -struct-fields

### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a>. When creating a signature, the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that corresponds to this algorithm is added to the <b>DigestInfo</b> element in the signature, and if this member is <b>NULL</b>, then the OID is not added. When verifying a signature, the verification fails if the OID that corresponds to this member is not the same as the OID in the signature. If there is no OID in the signature, then verification fails unless this member is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptverifysignature">BCryptVerifySignature</a>