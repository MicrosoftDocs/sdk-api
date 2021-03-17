---
UID: NS:wincrypt._CRYPT_TIMESTAMP_CONTEXT
title: CRYPT_TIMESTAMP_CONTEXT (wincrypt.h)
description: Contains both the encoded and decoded representations of a time stamp token.
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_CONTEXT","CRYPT_TIMESTAMP_CONTEXT","CRYPT_TIMESTAMP_CONTEXT structure [Security]","PCRYPT_TIMESTAMP_CONTEXT","PCRYPT_TIMESTAMP_CONTEXT structure pointer [Security]","security.crypt_timestamp_context","wincrypt/CRYPT_TIMESTAMP_CONTEXT","wincrypt/PCRYPT_TIMESTAMP_CONTEXT"]
old-location: security\crypt_timestamp_context.htm
tech.root: security
ms.assetid: 2831b2a9-0f84-4e41-a666-5903fc882965
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_CONTEXT, CRYPT_TIMESTAMP_CONTEXT, CRYPT_TIMESTAMP_CONTEXT structure [Security], PCRYPT_TIMESTAMP_CONTEXT, PCRYPT_TIMESTAMP_CONTEXT structure pointer [Security], security.crypt_timestamp_context, wincrypt/CRYPT_TIMESTAMP_CONTEXT, wincrypt/PCRYPT_TIMESTAMP_CONTEXT'
req.header: wincrypt.h
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
req.typenames: CRYPT_TIMESTAMP_CONTEXT, *PCRYPT_TIMESTAMP_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_CONTEXT
 - wincrypt/_CRYPT_TIMESTAMP_CONTEXT
 - PCRYPT_TIMESTAMP_CONTEXT
 - wincrypt/PCRYPT_TIMESTAMP_CONTEXT
 - CRYPT_TIMESTAMP_CONTEXT
 - wincrypt/CRYPT_TIMESTAMP_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_TIMESTAMP_CONTEXT
---

# CRYPT_TIMESTAMP_CONTEXT structure


## -description

The <b>CRYPT_TIMESTAMP_CONTEXT</b> structure contains both the encoded and decoded representations of a time stamp token.

## -struct-fields

### -field cbEncoded

The size, in bytes, of the buffer pointed to by the <b>pbEncoded</b> member.

### -field pbEncoded

A pointer to a buffer that contains an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded content information sequence. This value should be stored for future time stamp validations on the signature. Applications can use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function  with the <b>CERT_STORE_PROV_PKCS7</b> flag to find additional certificates or <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) related to the TSA time stamp signature.

### -field pTimeStamp

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_info">CRYPT_TIMESTAMP_INFO</a> structure that contains a signed data content type in Cryptographic Message Syntax (CMS) format.