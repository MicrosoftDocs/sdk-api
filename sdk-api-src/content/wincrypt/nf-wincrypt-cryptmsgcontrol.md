---
UID: NF:wincrypt.CryptMsgControl
title: CryptMsgControl function (wincrypt.h)
description: Performs a control operation after a message has been decoded by a final call to the CryptMsgUpdate function.
helpviewer_keywords: ["CMSG_CRYPT_RELEASE_CONTEXT_FLAG","CMSG_CTRL_ADD_ATTR_CERT","CMSG_CTRL_ADD_CERT","CMSG_CTRL_ADD_CMS_SIGNER_INFO","CMSG_CTRL_ADD_CRL","CMSG_CTRL_ADD_SIGNER","CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR","CMSG_CTRL_DECRYPT","CMSG_CTRL_DECRYPT","CMSG_CTRL_KEY_TRANS_DECRYPT","CMSG_CTRL_KEY_AGREE_DECRYPT","or CMSG_CTRL_MAIL_LIST_DECRYPT","and the streamed enveloped message is being decoded","CMSG_CTRL_DEL_ATTR_CERT","CMSG_CTRL_DEL_CERT","CMSG_CTRL_DEL_CRL","CMSG_CTRL_DEL_SIGNER","CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR","CMSG_CTRL_ENABLE_STRONG_SIGNATURE","CMSG_CTRL_KEY_AGREE_DECRYPT","CMSG_CTRL_KEY_TRANS_DECRYPT","CMSG_CTRL_MAIL_LIST_DECRYPT","CMSG_CTRL_VERIFY_HASH","CMSG_CTRL_VERIFY_SIGNATURE","CMSG_CTRL_VERIFY_SIGNATURE_EX","CryptMsgControl","CryptMsgControl function [Security]","_crypto2_cryptmsgcontrol","security.cryptmsgcontrol","wincrypt/CryptMsgControl"]
old-location: security\cryptmsgcontrol.htm
tech.root: security
ms.assetid: a990d44d-2993-429f-b817-2a834105ecef
ms.date: 12/05/2018
ms.keywords: CMSG_CRYPT_RELEASE_CONTEXT_FLAG, CMSG_CTRL_ADD_ATTR_CERT, CMSG_CTRL_ADD_CERT, CMSG_CTRL_ADD_CMS_SIGNER_INFO, CMSG_CTRL_ADD_CRL, CMSG_CTRL_ADD_SIGNER, CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR, CMSG_CTRL_DECRYPT, CMSG_CTRL_DECRYPT,CMSG_CTRL_KEY_TRANS_DECRYPT,CMSG_CTRL_KEY_AGREE_DECRYPT,or CMSG_CTRL_MAIL_LIST_DECRYPT,and the streamed enveloped message is being decoded, CMSG_CTRL_DEL_ATTR_CERT, CMSG_CTRL_DEL_CERT, CMSG_CTRL_DEL_CRL, CMSG_CTRL_DEL_SIGNER, CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR, CMSG_CTRL_ENABLE_STRONG_SIGNATURE, CMSG_CTRL_KEY_AGREE_DECRYPT, CMSG_CTRL_KEY_TRANS_DECRYPT, CMSG_CTRL_MAIL_LIST_DECRYPT, CMSG_CTRL_VERIFY_HASH, CMSG_CTRL_VERIFY_SIGNATURE, CMSG_CTRL_VERIFY_SIGNATURE_EX, CryptMsgControl, CryptMsgControl function [Security], _crypto2_cryptmsgcontrol, security.cryptmsgcontrol, wincrypt/CryptMsgControl
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
 - CryptMsgControl
 - wincrypt/CryptMsgControl
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
 - CryptMsgControl
---

# CryptMsgControl function


## -description

The <b>CryptMsgControl</b> function performs a control operation after a message has been decoded by a final 
call to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>  function. The control operations provided by this function are used for decryption, signature and hash verification, and the addition and deletion of certificates, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs), signers, and unauthenticated attributes.

Important changes that affect the handling of enveloped messages have been made to CryptoAPI to support <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability. For more information, see the Remarks for 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function.

## -parameters

### -param hCryptMsg [in]

A handle of a cryptographic message for which a control is to be applied.

### -param dwFlags [in]

The following value is defined when the <i>dwCtrlType</i> parameter is one of the following:

<ul>
<li>CMSG_CTRL_DECRYPT</li>
<li>CMSG_CTRL_KEY_TRANS_DECRYPT</li>
<li>CMSG_CTRL_KEY_AGREE_DECRYPT</li>
<li>CMSG_CTRL_MAIL_LIST_DECRYPT</li>
</ul>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_CRYPT_RELEASE_CONTEXT_FLAG"></a><a id="cmsg_crypt_release_context_flag"></a><dl>
<dt><b>CMSG_CRYPT_RELEASE_CONTEXT_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The handle to the cryptographic provider is released on the final call to the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function. This handle is not released if the  <b>CryptMsgControl</b> function  fails.

</td>
</tr>
</table>
 

If the <i>dwCtrlType</i> parameter does not specify a decrypt operation, set this value to zero.

### -param dwCtrlType [in]

The type of operation to be performed. Currently defined message control types and the type of structure that should be passed to the <i>pvCtrlPara</i> parameter are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_ATTR_CERT"></a><a id="cmsg_ctrl_add_attr_cert"></a><dl>
<dt><b>CMSG_CTRL_ADD_ATTR_CERT</b></dt>
<dt>14 (0xE)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>  that contains the encoded bytes of attribute certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_CERT"></a><a id="cmsg_ctrl_add_cert"></a><dl>
<dt><b>CMSG_CTRL_ADD_CERT</b></dt>
<dt>10 (0xA)</dt>
</dl>
</td>
<td width="60%">
A
								<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>   structure that contains the encoded bytes of the certificate to be added to the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_CMS_SIGNER_INFO"></a><a id="cmsg_ctrl_add_cms_signer_info"></a><dl>
<dt><b>CMSG_CTRL_ADD_CMS_SIGNER_INFO</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_cms_signer_info">CMSG_CMS_SIGNER_INFO</a> structure that contains signer information. This operation differs from <b>CMSG_CTRL_ADD_SIGNER</b> because the signer information contains the signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_CRL"></a><a id="cmsg_ctrl_add_crl"></a><dl>
<dt><b>CMSG_CTRL_ADD_CRL</b></dt>
<dt>12 (0xC)</dt>
</dl>
</td>
<td width="60%">
A BLOB  that contains the encoded bytes of the CRL to be added to the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_SIGNER"></a><a id="cmsg_ctrl_add_signer"></a><dl>
<dt><b>CMSG_CTRL_ADD_SIGNER</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a>   structure that contains the signer information to be added to the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR"></a><a id="cmsg_ctrl_add_signer_unauth_attr"></a><dl>
<dt><b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_ctrl_add_signer_unauth_attr_para">CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</a>   structure that contains the index of the signer and a BLOB  that contains the unauthenticated attribute information to be added to the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DECRYPT"></a><a id="cmsg_ctrl_decrypt"></a><dl>
<dt><b>CMSG_CTRL_DECRYPT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
A 
								<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para">CMSG_CTRL_DECRYPT_PARA</a>  structure used to decrypt the message for the specified key transport recipient. This value is applicable to RSA recipients.  This operation specifies that the <b>CryptMsgControl</b> function search the recipient index to obtain the key transport recipient information.  If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return  <b>CRYPT_E_INVALID_INDEX</b> if no key transport recipient is found.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_ATTR_CERT"></a><a id="cmsg_ctrl_del_attr_cert"></a><dl>
<dt><b>CMSG_CTRL_DEL_ATTR_CERT</b></dt>
<dt>15 (0xF)</dt>
</dl>
</td>
<td width="60%">
The index of the attribute certificate to be removed.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_CERT"></a><a id="cmsg_ctrl_del_cert"></a><dl>
<dt><b>CMSG_CTRL_DEL_CERT</b></dt>
<dt>11 (0xB)</dt>
</dl>
</td>
<td width="60%">
The index of the certificate to be deleted from the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_CRL"></a><a id="cmsg_ctrl_del_crl"></a><dl>
<dt><b>CMSG_CTRL_DEL_CRL</b></dt>
<dt>13 (0xD)</dt>
</dl>
</td>
<td width="60%">
The index of the CRL to be deleted from the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_SIGNER"></a><a id="cmsg_ctrl_del_signer"></a><dl>
<dt><b>CMSG_CTRL_DEL_SIGNER</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">
The index of the signer to be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR"></a><a id="cmsg_ctrl_del_signer_unauth_attr"></a><dl>
<dt><b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR</b></dt>
<dt>9 (0x9)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_ctrl_del_signer_unauth_attr_para">CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA</a>   structure that contains an index  that specifies the signer and the index  that specifies the signer's unauthenticated attribute to be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ENABLE_STRONG_SIGNATURE"></a><a id="cmsg_ctrl_enable_strong_signature"></a><dl>
<dt><b>CMSG_CTRL_ENABLE_STRONG_SIGNATURE</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure used to perform strong signature checking.

To check for a strong signature, specify this control type before calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetandverifysigner">CryptMsgGetAndVerifySigner</a> or before calling <b>CryptMsgControl</b> with the following control types set:

<ul>
<li><b>CMSG_CTRL_VERIFY_SIGNATURE</b></li>
<li><b>CMSG_CTRL_VERIFY_SIGNATURE_EX</b></li>
</ul>
After the signature is successfully verified, this function checks for a strong signature. If the signature is not strong, the operation will fail and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> value will be set to <b>NTE_BAD_ALGID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_KEY_AGREE_DECRYPT"></a><a id="cmsg_ctrl_key_agree_decrypt"></a><dl>
<dt><b>CMSG_CTRL_KEY_AGREE_DECRYPT</b></dt>
<dt>17 (0x11)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_key_agree_decrypt_para">CMSG_CTRL_KEY_AGREE_DECRYPT_PARA</a> structure used to decrypt the message for the specified key agreement session key. Key agreement is used with Diffie-Hellman encryption/decryption.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_KEY_TRANS_DECRYPT"></a><a id="cmsg_ctrl_key_trans_decrypt"></a><dl>
<dt><b>CMSG_CTRL_KEY_TRANS_DECRYPT</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_key_trans_decrypt_para">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure used to decrypt the message for the specified key transport recipient. Key transport is used with RSA encryption/decryption.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_MAIL_LIST_DECRYPT"></a><a id="cmsg_ctrl_mail_list_decrypt"></a><dl>
<dt><b>CMSG_CTRL_MAIL_LIST_DECRYPT</b></dt>
<dt>18 (0x12)</dt>
</dl>
</td>
<td width="60%">
A 
								<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_ctrl_mail_list_decrypt_para">CMSG_CTRL_MAIL_LIST_DECRYPT_PARA</a> structure used to decrypt the message for the specified recipient using a previously distributed key-encryption key (KEK).

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_VERIFY_HASH"></a><a id="cmsg_ctrl_verify_hash"></a><dl>
<dt><b>CMSG_CTRL_VERIFY_HASH</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
This value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_VERIFY_SIGNATURE"></a><a id="cmsg_ctrl_verify_signature"></a><dl>
<dt><b>CMSG_CTRL_VERIFY_SIGNATURE</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
A 
								<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>  structure that identifies the signer of the message whose signature is to be verified.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_VERIFY_SIGNATURE_EX"></a><a id="cmsg_ctrl_verify_signature_ex"></a><dl>
<dt><b>CMSG_CTRL_VERIFY_SIGNATURE_EX</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_ctrl_verify_signature_ex_para">CMSG_CTRL_VERIFY_SIGNATURE_EX_PARA</a>   structure that specifies the signer index and public key to verify the message signature. The signer public key can be a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure, a certificate context, or a certificate chain context.

</td>
</tr>
</table>

### -param pvCtrlPara [in]

A pointer to a structure determined by the value of <i>dwCtrlType</i>.

<table>
<tr>
<th><i>dwCtrlType</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DECRYPT__CMSG_CTRL_KEY_TRANS_DECRYPT__CMSG_CTRL_KEY_AGREE_DECRYPT__or_CMSG_CTRL_MAIL_LIST_DECRYPT__and_the_streamed_enveloped_message_is_being_decoded"></a><a id="cmsg_ctrl_decrypt__cmsg_ctrl_key_trans_decrypt__cmsg_ctrl_key_agree_decrypt__or_cmsg_ctrl_mail_list_decrypt__and_the_streamed_enveloped_message_is_being_decoded"></a><a id="CMSG_CTRL_DECRYPT__CMSG_CTRL_KEY_TRANS_DECRYPT__CMSG_CTRL_KEY_AGREE_DECRYPT__OR_CMSG_CTRL_MAIL_LIST_DECRYPT__AND_THE_STREAMED_ENVELOPED_MESSAGE_IS_BEING_DECODED"></a><dl>
<dt><b>CMSG_CTRL_DECRYPT, CMSG_CTRL_KEY_TRANS_DECRYPT, CMSG_CTRL_KEY_AGREE_DECRYPT, or CMSG_CTRL_MAIL_LIST_DECRYPT, and the streamed enveloped message is being decoded</b></dt>
</dl>
</td>
<td width="60%">
Decoding will be done as if the streamed content were being decrypted. If any encrypted streamed content has accumulated prior to this call, some or all of the <a href="/windows/desktop/SecGloss/p-gly">plaintext</a>  that results from the decryption of the cipher text is passed back to the application through the callback function specified in the call to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a> function.

<div class="alert"><b>Note</b>  When streaming an enveloped message, the <b>CryptMsgControl</b>  function is not called until the polling for the availability of the CMSG_ENVELOPE_ALGORITHM_PARAM succeeds. If the polling does not succeed, an error results. For a description of that polling, see 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a> function.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_VERIFY_HASH"></a><a id="cmsg_ctrl_verify_hash"></a><dl>
<dt><b>CMSG_CTRL_VERIFY_HASH</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/h-gly">hash</a> computed from the content of the message is compared against the hash contained in the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_ADD_SIGNER"></a><a id="cmsg_ctrl_add_signer"></a><dl>
<dt><b>CMSG_CTRL_ADD_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
<i>pvCtrlPara</i> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structure that contains the signer information to be added to the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_SIGNER"></a><a id="cmsg_ctrl_del_signer"></a><dl>
<dt><b>CMSG_CTRL_DEL_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
After a deletion is made, any other signer indices in use for this message are no longer valid and must be reacquired by calling 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR"></a><a id="cmsg_ctrl_del_signer_unauth_attr"></a><dl>
<dt><b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR</b></dt>
</dl>
</td>
<td width="60%">
After a deletion is made, any other unauthenticated attribute indices in use for this signer are no longer valid and must be reacquired by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_CERT"></a><a id="cmsg_ctrl_del_cert"></a><dl>
<dt><b>CMSG_CTRL_DEL_CERT</b></dt>
</dl>
</td>
<td width="60%">
After a deletion is made, any other certificate indices in use for this message are no longer valid and must be reacquired by calling 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CTRL_DEL_CRL"></a><a id="cmsg_ctrl_del_crl"></a><dl>
<dt><b>CMSG_CTRL_DEL_CRL</b></dt>
</dl>
</td>
<td width="60%">
After a deletion is made, any other CRL indices in use for this message are no longer valid and will need to be reacquired by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> function.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function   returns an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>. 

When a streamed, enveloped message is being decoded, errors encountered in the application-defined callback function specified by the <i>pStreamInfo</i>  parameter of the  
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a> function might be propagated to the <b>CryptMsgControl</b> function. If this happens, the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function is not called by the <b>CryptMsgControl</b> function after the callback function returns. This preserves any errors encountered under the control of the application. It is the responsibility of the callback function (or one of the APIs that it calls) to call the <b>SetLastError</b> function if an error occurs while the application is processing the streamed data.

Propagated errors might be encountered from the following functions:<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt">CryptDecrypt</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>
</li>
</ul>


The following  error codes are most commonly returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_ALREADY_DECRYPTED</b></dt>
</dl>
</td>
<td width="60%">
The message content has already been decrypted. This error can be returned if the <i>dwCtrlType</i> parameter is set to   CMSG_CTRL_DECRYPT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_AUTH_ATTR_MISSING</b></dt>
</dl>
</td>
<td width="60%">
The message does not contain an expected authenticated attribute. This error can be returned if the <i>dwCtrlType</i> parameter is set to   CMSG_CTRL_VERIFY_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_BAD_ENCODE</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered while encoding or decoding. This error can be returned if the <i>dwCtrlType</i>  parameter is set to  CMSG_CTRL_VERIFY_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_CONTROL_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The control type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_HASH_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The hash value is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_INVALID_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The index value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_INVALID_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The message type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_OID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The object identifier is badly formatted. This error can be returned if the <i>dwCtrlType</i>  parameter is set to  CMSG_CTRL_ADD_SIGNER.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_RECIPIENT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The enveloped data message does not contain the specified recipient. This error can be returned if the <i>dwCtrlType</i>  parameter is set to CMSG_CTRL_DECRYPT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_SIGNER_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified signer for the message was not found. This error can be returned if the <i>dwCtrlType</i>  parameter is set to  CMSG_CTRL_VERIFY_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
</dl>
</td>
<td width="60%">
The cryptographic algorithm is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected. This error can be returned if the <i>dwCtrlType</i>  parameter is set to  CMSG_CTRL_VERIFY_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid. This error can be returned if the <i>dwCtrlType</i> parameter is set to   CMSG_CTRL_DECRYPT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>