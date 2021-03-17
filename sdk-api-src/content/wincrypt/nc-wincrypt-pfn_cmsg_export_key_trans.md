---
UID: NC:wincrypt.PFN_CMSG_EXPORT_KEY_TRANS
title: PFN_CMSG_EXPORT_KEY_TRANS (wincrypt.h)
description: Encrypts and exports the content encryption key for a key transport recipient of an enveloped message.
helpviewer_keywords: ["PFN_CMSG_EXPORT_KEY_TRANS","PFN_CMSG_EXPORT_KEY_TRANS callback","PFN_CMSG_EXPORT_KEY_TRANS callback function [Security]","security.pfn_cmsg_export_key_trans","wincrypt/PFN_CMSG_EXPORT_KEY_TRANS"]
old-location: security\pfn_cmsg_export_key_trans.htm
tech.root: security
ms.assetid: bbb976df-5c8d-4d5e-ba92-7c534bba59de
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_EXPORT_KEY_TRANS, PFN_CMSG_EXPORT_KEY_TRANS callback, PFN_CMSG_EXPORT_KEY_TRANS callback function [Security], security.pfn_cmsg_export_key_trans, wincrypt/PFN_CMSG_EXPORT_KEY_TRANS
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
 - PFN_CMSG_EXPORT_KEY_TRANS
 - wincrypt/PFN_CMSG_EXPORT_KEY_TRANS
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
 - PFN_CMSG_EXPORT_KEY_TRANS
---

# PFN_CMSG_EXPORT_KEY_TRANS callback function


## -description

The <b>PFN_CMSG_EXPORT_KEY_TRANS</b> callback function encrypts and exports the content encryption key for a key transport recipient of an enveloped message. <b>PFN_CMSG_EXPORT_KEY_TRANS</b> can be installed by using a <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a> <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This function is called by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.

## -parameters

### -param pContentEncryptInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.

### -param pKeyTransEncodeInfo [in]

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_encode_info">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure that specifies the recipient public key used to encrypt the content encryption key.

### -param pKeyTransEncryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_trans_encrypt_info">CMSG_KEY_TRANS_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.

### -param dwFlags [in]

This value is not used. Set it to zero.

### -param pvReserved

This value is reserved. Set it to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>PFN_CMSG_EXPORT_KEY_TRANS</b> function must update the <b>EncryptedKey</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_trans_encrypt_info">CMSG_KEY_TRANS_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyTransEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory allocation for the encrypted key.

You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different OIDs. Which function is called depends on the value of the <b>fCNG</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>FALSE</td>
<td>CMSG_OID_EXPORT_KEY_TRANS_FUNC or CMSG_OID_CAPI1_EXPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllExportKeyTrans"</td>
</tr>
<tr>
<td>TRUE</td>
<td>CMSG_OID_CNG_EXPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllCNGExportKeyTrans"</td>
</tr>
</table>
