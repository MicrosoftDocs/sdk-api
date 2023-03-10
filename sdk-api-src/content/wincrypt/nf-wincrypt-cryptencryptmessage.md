---
UID: NF:wincrypt.CryptEncryptMessage
title: CryptEncryptMessage function (wincrypt.h)
description: The CryptEncryptMessage function encrypts and encodes a message.
helpviewer_keywords: ["CryptEncryptMessage","CryptEncryptMessage function [Security]","_crypto2_cryptencryptmessage","security.cryptencryptmessage","wincrypt/CryptEncryptMessage"]
old-location: security\cryptencryptmessage.htm
tech.root: security
ms.assetid: 927f2e9a-96cf-4744-bd57-420b5034d28d
ms.date: 12/05/2018
ms.keywords: CryptEncryptMessage, CryptEncryptMessage function [Security], _crypto2_cryptencryptmessage, security.cryptencryptmessage, wincrypt/CryptEncryptMessage
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptEncryptMessage
 - wincrypt/CryptEncryptMessage
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
 - CryptEncryptMessage
---

# CryptEncryptMessage function


## -description

The <b>CryptEncryptMessage</b> function <a href="/windows/desktop/SecGloss/e-gly">encrypts</a> and <a href="/windows/desktop/SecGloss/e-gly">encodes</a> a message.

## -parameters

### -param pEncryptPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encrypt_message_para">CRYPT_ENCRYPT_MESSAGE_PARA</a> structure that contains the encryption parameters.

The <b>CryptEncryptMessage</b> function does not support the SHA2 OIDs, <b>szOID_DH_SINGLE_PASS_STDDH_SHA256_KDF</b> and  <b>szOID_DH_SINGLE_PASS_STDDH_SHA384_KDF</b>.

### -param cRecipientCert [in]

Number of elements in the <i>rgpRecipientCert</i> array.

### -param rgpRecipientCert [in]

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures that contain the certificates of intended recipients of the message.

### -param pbToBeEncrypted [in]

A pointer to a buffer that contains the message that is to be encrypted.

### -param cbToBeEncrypted [in]

The size, in bytes, of the message that is to be encrypted.

### -param pbEncryptedBlob [out]

A pointer to <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains a buffer that receives the encrypted and encoded message. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbEncryptedBlob [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbEncryptedBlob</i> parameter. When the function returns, this variable contains the size, in bytes, of the encrypted and encoded message copied to <i>pbEncryptedBlob</i>. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer of the <i>pbEncryptedBlob</i>, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencrypt">CryptEncrypt</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> can be propagated to this function.</div>
<div> </div>
The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the following error codes most often.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbEncryptedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncryptedBlob</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pEncryptPara</i> is not valid.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>