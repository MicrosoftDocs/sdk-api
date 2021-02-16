---
UID: NS:wincrypt._CMSG_CNG_CONTENT_DECRYPT_INFO
title: CMSG_CNG_CONTENT_DECRYPT_INFO (wincrypt.h)
description: Contains all the relevant information passed between CryptMsgControl and object identifier (OID) installable functions for the import and decryption of a Cryptography API:\_Next Generation (CNG) content encryption key (CEK).
helpviewer_keywords: ["*PCMSG_CNG_CONTENT_DECRYPT_INFO","CMSG_CNG_CONTENT_DECRYPT_INFO","CMSG_CNG_CONTENT_DECRYPT_INFO structure [Security]","PCMSG_CNG_CONTENT_DECRYPT_INFO","PCMSG_CNG_CONTENT_DECRYPT_INFO structure pointer [Security]","security.cmsg_cng_content_decrypt_info","wincrypt/CMSG_CNG_CONTENT_DECRYPT_INFO","wincrypt/PCMSG_CNG_CONTENT_DECRYPT_INFO"]
old-location: security\cmsg_cng_content_decrypt_info.htm
tech.root: security
ms.assetid: 56e94b20-9d0a-4694-973f-a5878ad54f48
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CNG_CONTENT_DECRYPT_INFO, CMSG_CNG_CONTENT_DECRYPT_INFO, CMSG_CNG_CONTENT_DECRYPT_INFO structure [Security], PCMSG_CNG_CONTENT_DECRYPT_INFO, PCMSG_CNG_CONTENT_DECRYPT_INFO structure pointer [Security], security.cmsg_cng_content_decrypt_info, wincrypt/CMSG_CNG_CONTENT_DECRYPT_INFO, wincrypt/PCMSG_CNG_CONTENT_DECRYPT_INFO'
req.header: wincrypt.h
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
req.typenames: CMSG_CNG_CONTENT_DECRYPT_INFO, *PCMSG_CNG_CONTENT_DECRYPT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CNG_CONTENT_DECRYPT_INFO
 - wincrypt/_CMSG_CNG_CONTENT_DECRYPT_INFO
 - PCMSG_CNG_CONTENT_DECRYPT_INFO
 - wincrypt/PCMSG_CNG_CONTENT_DECRYPT_INFO
 - CMSG_CNG_CONTENT_DECRYPT_INFO
 - wincrypt/CMSG_CNG_CONTENT_DECRYPT_INFO
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
 - CMSG_CNG_CONTENT_DECRYPT_INFO
---

# CMSG_CNG_CONTENT_DECRYPT_INFO structure


## -description

The <b>CMSG_CNG_CONTENT_DECRYPT_INFO</b> structure contains all the relevant information passed between <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> and <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) installable functions for the import and decryption of a Cryptography API: Next Generation (CNG) content encryption key (CEK). The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> function uses this structure to call the following functions:<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans">PFN_CMSG_CNG_IMPORT_KEY_TRANS</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree">PFN_CMSG_CNG_IMPORT_KEY_AGREE</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key">PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</a>
</li>
</ul>

## -struct-fields

### -field cbSize

Contains the size, in bytes, of this structure.

### -field ContentEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>   structure that specifies the algorithm used to encrypt the message contents and any associated parameters.

### -field pfnAlloc

A pointer to an installable function used to allocate memory for any updated member.

### -field pfnFree

A pointer to an installable function used to free memory allocated by <i>pfnAlloc</i>.

### -field hNCryptKey

A handle to the CNG <a href="/windows/desktop/SecGloss/p-gly">private key</a> to be used for decryption of the CEK contained in the <i>pKeyTransDecryptPara</i> parameter or the <i>pKeyAgreeDecryptPara</i> parameter of the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans">PFN_CMSG_CNG_IMPORT_KEY_TRANS</a> function. Callback functions must use this key instead of the one contained in the <i>DecryptPara</i> structure because that structure might contain a converted <b>HCRYPTPROV</b> handle.

### -field pbContentEncryptKey

Using the <b>hNCryptKey</b> member, the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans">PFN_CMSG_CNG_IMPORT_KEY_TRANS</a> function must update this member by decrypting the CEK in the <i>pKeyTransDecryptPara</i> parameter or the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree">PFN_CMSG_CNG_IMPORT_KEY_AGREE</a> function must update this member by decrypting the EncryptedKey in the <i>pKeyAgreeDecryptPara</i> parameter. The memory for this member must be allocated by using the <b>pfnAlloc</b> member. The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key">PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</a> function will use these bytes as the secret to generate the <b>hCNGContentEncryptKey</b> member. Even for an error, you must free and zero any allocated memory by using the <b>pfnFree</b> member.

### -field cbContentEncryptKey

The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans">PFN_CMSG_CNG_IMPORT_KEY_TRANS</a> or <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree">PFN_CMSG_CNG_IMPORT_KEY_AGREE</a> function must update this member with the size, in bytes, of the above <b>pbContentEncryptKey</b> member.

### -field hCNGContentEncryptKey

The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key">PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</a> function must update this member with the generated <b>BCRYPT_KEY_HANDLE</b> to be used for content decryption. Even for an error, you must release this handle by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -field pbCNGContentEncryptKeyObject

The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key">PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</a> function must update this member with the memory allocated by the <b>pfnAlloc</b> member to be associated with the <b>hCNGContentEncryptKey</b> member. Even for an error, you must free and zero any allocated memory by using the <b>pfnFree</b> member.