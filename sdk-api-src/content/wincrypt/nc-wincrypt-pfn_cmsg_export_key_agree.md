---
UID: NC:wincrypt.PFN_CMSG_EXPORT_KEY_AGREE
title: PFN_CMSG_EXPORT_KEY_AGREE (wincrypt.h)
description: Encrypts and exports the content encryption key for a key agreement recipient of an enveloped message.
helpviewer_keywords: ["PFN_CMSG_EXPORT_KEY_AGREE","PFN_CMSG_EXPORT_KEY_AGREE callback","PFN_CMSG_EXPORT_KEY_AGREE callback function [Security]","security.pfn_cmsg_export_key_agree","wincrypt/PFN_CMSG_EXPORT_KEY_AGREE"]
old-location: security\pfn_cmsg_export_key_agree.htm
tech.root: security
ms.assetid: 5283f3be-7451-4896-82a5-bcfe63db9344
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_EXPORT_KEY_AGREE, PFN_CMSG_EXPORT_KEY_AGREE callback, PFN_CMSG_EXPORT_KEY_AGREE callback function [Security], security.pfn_cmsg_export_key_agree, wincrypt/PFN_CMSG_EXPORT_KEY_AGREE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CMSG_EXPORT_KEY_AGREE
 - wincrypt/PFN_CMSG_EXPORT_KEY_AGREE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CMSG_EXPORT_KEY_AGREE
---

# PFN_CMSG_EXPORT_KEY_AGREE callback function


## -description

The <b>PFN_CMSG_EXPORT_KEY_AGREE</b> callback function encrypts and exports the content encryption key for a key agreement recipient of an enveloped message. <b>PFN_CMSG_EXPORT_KEY_AGREE</b> can be installed by using a <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a> <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This function is called by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.

## -parameters

### -param pContentEncryptInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.

### -param pKeyAgreeEncodeInfo [in]

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_key_agree_recipient_encode_info">CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</a> structure that specifies the key used to encrypt the content encryption key.

### -param pKeyAgreeEncryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_encrypt_info">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.

### -param dwFlags [in]

This value is not used. Set it to zero.

### -param pvReserved

This parameter is reserved and must be NULL.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For each recipient key, the <b>PFN_CMSG_EXPORT_KEY_AGREE</b> function must update the   <b>EncryptedKey</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_key_encrypt_info">CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</a> structure referred to by the <b>rgpKeyAgreeKeyEncryptInfo</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_encrypt_info">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyAgreeEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory for any values that it updates.

If, upon entry,  the <b>dwEncryptFlags</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> member is set to <b>CMSG_CONTENT_ENCRYPT_PAD_ENCODED_LEN_FLAG</b>, the ephemeral <b>PublicKey</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure referred to by the <b>OriginatorPublicKeyInfo</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_encrypt_info">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyAgreeEncryptInfo</i> parameter should be padded with zeros to always obtain the same maximum encoded length. <div class="alert"><b>Note</b>  The length of the generated ephemeral Y public key can vary depending on the number of leading zero bits.</div>
<div> </div>


You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different OIDs. Which function is called depends on the value of the  <b>fCNG</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>CMSG_OID_EXPORT_KEY_AGREE_FUNC or CMSG_OID_CAPI1_EXPORT_KEY_AGREE_FUNC</td>
<td>"CryptMsgDllExportKeyAgree"</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>CMSG_OID_CNG_EXPORT_KEY_AGREE_FUNC</td>
<td>"CryptMsgDllCNGExportKeyAgree"</td>
</tr>
</table>
