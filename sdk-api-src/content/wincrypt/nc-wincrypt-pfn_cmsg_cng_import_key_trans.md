---
UID: NC:wincrypt.PFN_CMSG_CNG_IMPORT_KEY_TRANS
title: PFN_CMSG_CNG_IMPORT_KEY_TRANS (wincrypt.h)
description: Imports and decrypts a content encryption key (CEK) that is intended for a key transport recipient.
helpviewer_keywords: ["PFN_CMSG_CNG_IMPORT_KEY_TRANS","PFN_CMSG_CNG_IMPORT_KEY_TRANS callback","PFN_CMSG_CNG_IMPORT_KEY_TRANS callback function [Security]","security.pfn_cmsg_cng_import_key_trans","wincrypt/PFN_CMSG_CNG_IMPORT_KEY_TRANS"]
old-location: security\pfn_cmsg_cng_import_key_trans.htm
tech.root: security
ms.assetid: e03d86e3-4ace-4425-8aae-e3b4721cb9cc
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_CNG_IMPORT_KEY_TRANS, PFN_CMSG_CNG_IMPORT_KEY_TRANS callback, PFN_CMSG_CNG_IMPORT_KEY_TRANS callback function [Security], security.pfn_cmsg_cng_import_key_trans, wincrypt/PFN_CMSG_CNG_IMPORT_KEY_TRANS
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CMSG_CNG_IMPORT_KEY_TRANS
 - wincrypt/PFN_CMSG_CNG_IMPORT_KEY_TRANS
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
 - PFN_CMSG_CNG_IMPORT_KEY_TRANS
---

# PFN_CMSG_CNG_IMPORT_KEY_TRANS callback function


## -description

The <b>PFN_CMSG_CNG_IMPORT_KEY_TRANS</b> callback function imports and decrypts a content encryption key (CEK) that is intended for a key transport recipient. <b>PFN_CMSG_CNG_IMPORT_KEY_TRANS</b> can be installed by using a Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param pCNGContentDecryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_cng_content_decrypt_info">CMSG_CNG_CONTENT_DECRYPT_INFO</a> structure to be updated with the decrypted CEK bytes. This parameter contains the key used to decrypt the CEK.
The following <i>pKeyTransDecryptPara</i> parameter contains the 	CEK bytes to be decrypted.

### -param pKeyTransDecryptPara [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_key_trans_decrypt_para">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure that contains the key transport information passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> function in the <b>CMSG_CTRL_DECRYPT</b> or <b>CMSG_CTRL_KEY_TRANS_DECRYPT</b> cases. For the <b>CMSG_CTRL_DECRYPT</b> case, <b>CryptMsgControl</b> converts the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para">CMSG_CTRL_DECRYPT_PARA</a> structure to a <b>CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</b> structure. 

The
<b>EncryptedKey</b> member of the <b>pKeyTrans</b> member contains the CEK bytes to be decrypted. Because a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_key_trans_decrypt_para">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure might contain an <b>HCRYPTPROV</b> choice, its <b>hNCryptKey</b> member must not be used to decrypt <b>EncryptedKey</b>. Instead, you must use the <b>hNCryptKey</b> specified in the <i>pCNGContentDecryptInfo</i> parameter.


This function must not update members of the  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_key_trans_decrypt_para">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure.

### -param dwFlags [in]

This parameter is reserved. Set it to zero.

### -param pvReserved

This parameter is reserved. Set it to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



If this callback function does not support the key encryption algorithm, it must return <b>FALSE</b> and call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with ERROR_NOT_SUPPORTED.

## -remarks

The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> function calls this function for the following operations specified by the <i>dwCtrlType</i> parameter:

<b>CMSG_CTRL_DECRYPT</b>
<b>CMSG_CTRL_KEY_TRANS_DECRYPT</b>
You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_CNG_IMPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllCNGImportKeyTrans"</td>
</tr>
</table>
 


#### Examples

For an example that deploys an OID-installable callback function, see <a href="/windows/desktop/SecCrypto/extending-cryptoapi-functionality">Extending CryptoAPI Functionality</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecCrypto/decoding-enveloped-data">Decoding Enveloped Data</a>
