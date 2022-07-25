---
UID: NC:wincrypt.PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY
title: PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY (wincrypt.h)
description: Imports an already decrypted content encryption key (CEK).
helpviewer_keywords: ["PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY","PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY callback","PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY callback function [Security]","security.pfn_cmsg_cng_import_content_encrypt_key","wincrypt/PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY"]
old-location: security\pfn_cmsg_cng_import_content_encrypt_key.htm
tech.root: security
ms.assetid: cb410582-68bd-43ed-b65f-17a7c1e0800f
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY, PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY callback, PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY callback function [Security], security.pfn_cmsg_cng_import_content_encrypt_key, wincrypt/PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY
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
 - PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY
 - wincrypt/PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY
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
 - PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY
---

# PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY callback function


## -description

The <b>PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</b> callback function imports an already decrypted content encryption key (CEK).  The <b>PFN_CMSG_CNG_IMPORT_CONTENT_ENCRYPT_KEY</b> function can be installed by using a Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param pCNGContentDecryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_cng_content_decrypt_info">CMSG_CNG_CONTENT_DECRYPT_INFO</a> structure to be updated with the imported CEK. This structure contains all the relevant information passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> function.

### -param dwFlags [in]

This parameter is reserved. Set it to zero.

### -param pvReserved

This parameter is reserved. Set it to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



If this callback function does not support the key encryption algorithm, it must return <b>FALSE</b> and call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with ERROR_NOT_SUPPORTED.

## -remarks

The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> function calls this function for the following operations specified by its <i>dwCtrlType</i> parameter:<dl>
<dd><b>CMSG_CTRL_DECRYPT</b></dd>
<dd><b>CMSG_CTRL_KEY_TRANS_DECRYPT</b></dd>
<dd><b>CMSG_CTRL_KEY_AGREE_DECRYPT</b></dd>
</dl>


You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_CNG_IMPORT_CONTENT_ENCRYPT_KEY_FUNC</td>
<td>"CryptMsgDllCNGImportContentEncryptKey"</td>
</tr>
</table>
 


#### Examples

For an example that deploys an OID-installable callback function, see <a href="/windows/desktop/SecCrypto/extending-cryptoapi-functionality">Extending CryptoAPI Functionality</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecCrypto/decoding-enveloped-data">Decoding Enveloped Data</a>
