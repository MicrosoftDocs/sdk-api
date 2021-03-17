---
UID: NF:wincrypt.CryptDecodeMessage
title: CryptDecodeMessage function (wincrypt.h)
description: Decodes, decrypts, and verifies a cryptographic message.
helpviewer_keywords: ["CryptDecodeMessage","CryptDecodeMessage function [Security]","_crypto2_cryptdecodemessage","security.cryptdecodemessage","wincrypt/CryptDecodeMessage"]
old-location: security\cryptdecodemessage.htm
tech.root: security
ms.assetid: 25ffd058-8f75-4ba5-b075-e3efc09f5d9d
ms.date: 12/05/2018
ms.keywords: CryptDecodeMessage, CryptDecodeMessage function [Security], _crypto2_cryptdecodemessage, security.cryptdecodemessage, wincrypt/CryptDecodeMessage
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
 - CryptDecodeMessage
 - wincrypt/CryptDecodeMessage
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
 - CryptDecodeMessage
---

# CryptDecodeMessage function


## -description

The <b>CryptDecodeMessage</b> function decodes, decrypts, and verifies a cryptographic message.

This function can be used when the type of cryptographic message is unknown. The <i>dwMsgTypeFlags</i> constants can be combined with a bitwise-<b>OR</b> operation so that the function will try to find one of the types. When one of the types is found, the function reports the type found and returns the data appropriate to that type.

In each pass, the function cracks only a single level of encryption or encoding. For additional cracking, this function, or one of the other 
<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>, must be called again.

## -parameters

### -param dwMsgTypeFlags [in]

Indicates the message type. Message types can be combined with the bitwise-<b>OR</b> operator. This parameter can be one of the following message types:

<ul>
<li>CMSG_DATA_FLAG</li>
<li>CMSG_SIGNED_FLAG</li>
<li>CMSG_ENVELOPED_FLAG</li>
<li>CMSG_SIGNED_AND_ENVELOPED_FLAG</li>
<li>CMSG_HASHED_FLAG</li>
</ul>
<div class="alert"><b>Note</b>  After return, the <b>DWORD</b> pointed to by <i>pdwMsgType</i> is set with the type of the message.</div>
<div> </div>

### -param pDecryptPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_decrypt_message_para">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains  decryption parameters.

### -param pVerifyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure that contains   verification parameters.

### -param dwSignerIndex [in]

Indicates which signer, among the possible many signers of a message, is to be verified. This index can be changed in multiple calls to the function to verify additional signers. 




<i>dwSignerIndex</i> is set to zero for the first signer. If the function returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call returned the last signer of the message. This parameter is used only with messages of types CMSG_SIGNED_AND_ENVELOPED or CMSG_SIGNED. For all other message types, it should be set to zero.

### -param pbEncodedBlob [in]

A pointer to the encoded <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that is to be decoded.

### -param cbEncodedBlob [in]

The size, in bytes, of the encoded BLOB.

### -param dwPrevInnerContentType [in]

Only applicable when processing nested cryptographic messages. When processing an outer cryptographic message, it must be set to zero. When decoding a nested cryptographic message, it is set to the value returned at <i>pdwInnerContentType</i> by a previous calling of 
<b>CryptDecodeMessage</b> for the outer message. It can be any of the CMSG types listed in <i>pdwMsgType</i>. For backward compatibility, set <i>dwPrevInnerContentType</i> to zero.

### -param pdwMsgType [out, optional]

A pointer to a <b>DWORD</b> that specifies the message type returned. This parameter can be one of the following message types:

<ul>
<li>CMSG_DATA</li>
<li>CMSG_SIGNED</li>
<li>CMSG_ENVELOPED</li>
<li>CMSG_SIGNED_AND_ENVELOPED</li>
<li>CMSG_HASHED</li>
</ul>

### -param pdwInnerContentType [out, optional]

A pointer to a <b>DWORD</b> that specifies the type of an inner message. The message type codes used for <i>pdwMsgType</i> are used here, also. 




If there is no cryptographic nesting, CMSG_DATA is returned.

### -param pbDecoded [out, optional]

A pointer to a buffer to receive the decoded message. 




This parameter can be <b>NULL</b> if the decoded message is not required or to set the size of the decoded message for memory allocation purposes. A decoded message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbDecoded [in, out, optional]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecoded</i> parameter. When the function returns, this variable contains the size of the decoded message. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure with a certificate that corresponds to the private <a href="/windows/desktop/SecGloss/e-gly">exchange key</a> needed to decode the message. This parameter is only set for message types CMSG_ENVELOPED and CMSG_SIGNED_AND_ENVELOPED.

### -param ppSignerCert [out, optional]

A pointer to a 
pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> of the signer. This parameter is only set for message types CMSG_SIGNED and CMSG_SIGNED_AND_ENVELOPED.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>, or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagehash">CryptVerifyMessageHash</a> functions can be propagated to this function.

The following error code is most commonly returned by the 
		       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

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
If the buffer specified by the <i>pbDecoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbDecoded</i>.

</td>
</tr>
</table>

## -remarks

The <i>dwMsgTypeFlags</i> parameter specifies the set of allowable messages. For example, to decode either SIGNED or ENVELOPED messages, set <i>dwMsgTypeFlags</i> to CMSG_SIGNED_FLAG | CMSG_ENVELOPED_FLAG. Either or both of the <i>pDecryptPara</i> or <i>pVerifyPara</i> parameters must be specified.

For a successfully decoded or verified message, the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> pointers pointed to by <i>ppXchgCert</i> and <i>ppSignerCert</i> are updated. They must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. If the function fails, they are set to <b>NULL</b>.

The <i>ppXchgCert</i> or <i>ppSignerCert</i> parameters can be set to <b>NULL</b> before the function is called, which indicates that the caller is not interested in getting the exchange certificate or the signer <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagehash">CryptVerifyMessageHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>