---
UID: NS:wincrypt._CMSG_CTRL_KEY_TRANS_DECRYPT_PARA
title: CMSG_CTRL_KEY_TRANS_DECRYPT_PARA (wincrypt.h)
description: Contains information about a key transport message recipient.
helpviewer_keywords: ["*PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA","CMSG_CTRL_KEY_TRANS_DECRYPT_PARA","CMSG_CTRL_KEY_TRANS_DECRYPT_PARA structure [Security]","PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA","PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA structure pointer [Security]","_crypto2_cmsg_ctrl_key_trans_decrypt_para","security.cmsg_ctrl_key_trans_decrypt_para","wincrypt/CMSG_CTRL_KEY_TRANS_DECRYPT_PARA","wincrypt/PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA"]
old-location: security\cmsg_ctrl_key_trans_decrypt_para.htm
tech.root: security
ms.assetid: 5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA, CMSG_CTRL_KEY_TRANS_DECRYPT_PARA, CMSG_CTRL_KEY_TRANS_DECRYPT_PARA structure [Security], PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA, PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA structure pointer [Security], _crypto2_cmsg_ctrl_key_trans_decrypt_para, security.cmsg_ctrl_key_trans_decrypt_para, wincrypt/CMSG_CTRL_KEY_TRANS_DECRYPT_PARA, wincrypt/PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA'
f1_keywords:
- wincrypt/CMSG_CTRL_KEY_TRANS_DECRYPT_PARA
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincrypt.h
api_name:
- CMSG_CTRL_KEY_TRANS_DECRYPT_PARA
targetos: Windows
req.typenames: CMSG_CTRL_KEY_TRANS_DECRYPT_PARA, *PCMSG_CTRL_KEY_TRANS_DECRYPT_PARA
req.redist: 
ms.custom: 19H1
---

# CMSG_CTRL_KEY_TRANS_DECRYPT_PARA structure


## -description


The <b>CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</b> structure contains information about a key transport message recipient.


## -struct-fields




### -field cbSize

The size, in bytes, of this data structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hCryptProv

A handle to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) used to do the recipient key encryption and export. If <b>NULL</b>, the provider specified in <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> is used.
					The CNG function <a href="https://docs.microsoft.com/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> is called to determine the union choice.


### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG CSP used to do the recipient key encryption and export. The CNG function <a href="https://docs.microsoft.com/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function <a href="https://docs.microsoft.com/windows/desktop/api/ncrypt/nf-ncrypt-ncrypttranslatehandle">NCryptTranslateHandle</a> will be called to convert the CryptoAPI CSP <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="https://docs.microsoft.com/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function.


### -field dwKeySpec

Specifies the encrypted key. The encrypted key is the result of encrypting the content-encryption key for a specific recipient by using that recipient's public key. This member is not used when the <i>hNCryptKey</i> member is used.


### -field pKeyTrans

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_info">CMSG_KEY_TRANS_RECIPIENT_INFO</a> structure.


### -field dwRecipientIndex

Indicates a specific recipient in any array of recipients.

