---
UID: NS:wincrypt._CMSG_HASHED_ENCODE_INFO
title: CMSG_HASHED_ENCODE_INFO (wincrypt.h)
description: Used with hashed messages. It is passed to the CryptMsgOpenToEncode function if the CryptMsgOpenToEncode function's dwMsgType parameter is CMSG_ENVELOPED.
helpviewer_keywords: ["*PCMSG_HASHED_ENCODE_INFO","CMSG_HASHED_ENCODE_INFO","CMSG_HASHED_ENCODE_INFO structure [Security]","PCMSG_HASHED_ENCODE_INFO","PCMSG_HASHED_ENCODE_INFO structure pointer [Security]","_crypto2_cmsg_hashed_encode_info","security.cmsg_hashed_encode_info","wincrypt/CMSG_HASHED_ENCODE_INFO","wincrypt/PCMSG_HASHED_ENCODE_INFO"]
old-location: security\cmsg_hashed_encode_info.htm
tech.root: security
ms.assetid: 05dfeda0-a8a1-4203-a68a-af92903ab215
ms.date: 12/05/2018
ms.keywords: '*PCMSG_HASHED_ENCODE_INFO, CMSG_HASHED_ENCODE_INFO, CMSG_HASHED_ENCODE_INFO structure [Security], PCMSG_HASHED_ENCODE_INFO, PCMSG_HASHED_ENCODE_INFO structure pointer [Security], _crypto2_cmsg_hashed_encode_info, security.cmsg_hashed_encode_info, wincrypt/CMSG_HASHED_ENCODE_INFO, wincrypt/PCMSG_HASHED_ENCODE_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CMSG_HASHED_ENCODE_INFO, *PCMSG_HASHED_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_HASHED_ENCODE_INFO
 - wincrypt/_CMSG_HASHED_ENCODE_INFO
 - PCMSG_HASHED_ENCODE_INFO
 - wincrypt/PCMSG_HASHED_ENCODE_INFO
 - CMSG_HASHED_ENCODE_INFO
 - wincrypt/CMSG_HASHED_ENCODE_INFO
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
 - CMSG_HASHED_ENCODE_INFO
---

# CMSG_HASHED_ENCODE_INFO structure


## -description

The <b>CMSG_HASHED_ENCODE_INFO</b> structure is used with <a href="/windows/desktop/SecGloss/h-gly">hashed</a> messages. It is passed to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function if the <b>CryptMsgOpenToEncode</b> function's <i>dwMsgType</i> parameter is <b>CMSG_ENVELOPED</b>.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Specifies a handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) used to do the hash. The <i>hCryptProv</i> private keys are not used. 


This member's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, pass zero to use the default RSA or DSS provider to be acquired before doing hash, signature verification, or recipient encryption operations.

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the hash algorithm type and any associated additional parameters.

### -field pvHashAuxInfo

This member is currently not used and must be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>