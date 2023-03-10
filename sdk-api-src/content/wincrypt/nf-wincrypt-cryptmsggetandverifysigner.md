---
UID: NF:wincrypt.CryptMsgGetAndVerifySigner
title: CryptMsgGetAndVerifySigner function (wincrypt.h)
description: The CryptMsgGetAndVerifySigner function verifies a cryptographic message's signature.
helpviewer_keywords: ["CMSG_SIGNER_ONLY_FLAG","CMSG_TRUSTED_SIGNER_FLAG","CMSG_USE_SIGNER_INDEX_FLAG","CryptMsgGetAndVerifySigner","CryptMsgGetAndVerifySigner function [Security]","_crypto2_cryptmsggetandverifysigner","security.cryptmsggetandverifysigner","wincrypt/CryptMsgGetAndVerifySigner"]
old-location: security\cryptmsggetandverifysigner.htm
tech.root: security
ms.assetid: 380c9cf3-27a2-4354-b1c8-97cec33f4e44
ms.date: 12/05/2018
ms.keywords: CMSG_SIGNER_ONLY_FLAG, CMSG_TRUSTED_SIGNER_FLAG, CMSG_USE_SIGNER_INDEX_FLAG, CryptMsgGetAndVerifySigner, CryptMsgGetAndVerifySigner function [Security], _crypto2_cryptmsggetandverifysigner, security.cryptmsggetandverifysigner, wincrypt/CryptMsgGetAndVerifySigner
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptMsgGetAndVerifySigner
 - wincrypt/CryptMsgGetAndVerifySigner
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptMsgGetAndVerifySigner
---

# CryptMsgGetAndVerifySigner function


## -description

The <b>CryptMsgGetAndVerifySigner</b> function verifies a cryptographic message's signature.

## -parameters

### -param hCryptMsg [in]

Handle of a cryptographic message.

### -param cSignerStore [in]

Number of stores in the <i>rghSignerStore</i> array.

### -param rghSignerStore [in, optional]

Array of certificate store handles that can be searched for a signer's certificate.

### -param dwFlags [in]

Indicates particular use of the function. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_TRUSTED_SIGNER_FLAG"></a><a id="cmsg_trusted_signer_flag"></a><dl>
<dt><b>CMSG_TRUSTED_SIGNER_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The stores in <i>rghSignerStore</i> are assumed trusted and they are the only stores searched to find the certificate corresponding to the signer's issuer and serial number. Otherwise, signer stores can be provided to supplement the message's store of certificates. If a signer certificate is found, its public key is used to verify the message signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_ONLY_FLAG"></a><a id="cmsg_signer_only_flag"></a><dl>
<dt><b>CMSG_SIGNER_ONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Return the signer without doing the signature verification.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_USE_SIGNER_INDEX_FLAG"></a><a id="cmsg_use_signer_index_flag"></a><dl>
<dt><b>CMSG_USE_SIGNER_INDEX_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Only the signer specified by *<i>pdwSignerIndex</i> is returned. Otherwise, iterate through all the signers until a signature is verified or there are no more signers.

</td>
</tr>
</table>

### -param ppSigner [out, optional]

If the signature is verified, <i>ppSigner</i> is updated to point to the signer's <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>. When you have finished using the certificate, free the context by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function. This parameter can be <b>NULL</b> if the application has no need for the signer's certificate.

### -param pdwSignerIndex [in, out, optional]

If the signature is verified, <i>pdwSigner</i> is updated to point to the index of the signer in the array of signers. This parameter can be <b>NULL</b> if the application has no need for the index of the signer.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Verification Functions Using CTLs</a>