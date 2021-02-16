---
UID: NS:wincrypt._CMSG_CMS_SIGNER_INFO
title: CMSG_CMS_SIGNER_INFO (wincrypt.h)
description: Contains the content of the defined SignerInfo in signed or signed and enveloped messages.
helpviewer_keywords: ["*PCMSG_CMS_SIGNER_INFO","CMSG_CMS_SIGNER_INFO","CMSG_CMS_SIGNER_INFO structure [Security]","PCMSG_CMS_SIGNER_INFO","PCMSG_CMS_SIGNER_INFO structure pointer [Security]","_crypto2_cmsg_cms_signer_info","security.cmsg_cms_signer_info","wincrypt/CMSG_CMS_SIGNER_INFO","wincrypt/PCMSG_CMS_SIGNER_INFO"]
old-location: security\cmsg_cms_signer_info.htm
tech.root: security
ms.assetid: 177323ef-4e26-4681-a474-1a99fb6900af
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CMS_SIGNER_INFO, CMSG_CMS_SIGNER_INFO, CMSG_CMS_SIGNER_INFO structure [Security], PCMSG_CMS_SIGNER_INFO, PCMSG_CMS_SIGNER_INFO structure pointer [Security], _crypto2_cmsg_cms_signer_info, security.cmsg_cms_signer_info, wincrypt/CMSG_CMS_SIGNER_INFO, wincrypt/PCMSG_CMS_SIGNER_INFO'
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
req.typenames: CMSG_CMS_SIGNER_INFO, *PCMSG_CMS_SIGNER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CMS_SIGNER_INFO
 - wincrypt/_CMSG_CMS_SIGNER_INFO
 - PCMSG_CMS_SIGNER_INFO
 - wincrypt/PCMSG_CMS_SIGNER_INFO
 - CMSG_CMS_SIGNER_INFO
 - wincrypt/CMSG_CMS_SIGNER_INFO
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
 - CMSG_CMS_SIGNER_INFO
---

# CMSG_CMS_SIGNER_INFO structure


## -description

The <b>CMSG_CMS_SIGNER_INFO</b> structure contains the content of the defined SignerInfo in signed or signed and enveloped messages. In decoding a received message, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> is called for each signer to get a <b>CMSG_CMS_SIGNER_INFO</b> structure.

## -struct-fields

### -field dwVersion

The version of this structure.

### -field SignerId

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure that identifies the signer's certificate.

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used in generating the hash of a message.

### -field HashEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to encrypt the hash.

### -field EncryptedHash

A
						<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the encrypted hash of the message, the signature.

### -field AuthAttrs

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure that contains authenticated attributes of the signer.

### -field UnauthAttrs

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure that contains unauthenticated attributes of the signer.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>