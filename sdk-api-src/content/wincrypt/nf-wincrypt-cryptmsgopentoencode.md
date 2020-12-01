---
UID: NF:wincrypt.CryptMsgOpenToEncode
title: CryptMsgOpenToEncode function (wincrypt.h)
description: Opens a cryptographic message for encoding and returns a handle of the opened message.
helpviewer_keywords: ["CMSG_AUTHENTICATED_ATTRIBUTES_FLAG","CMSG_BARE_CONTENT_FLAG","CMSG_CMS_ENCAPSULATED_CONTENT_FLAG","CMSG_CONTENTS_OCTETS_FLAG","CMSG_CRYPT_RELEASE_CONTEXT_FLAG","CMSG_DATA","CMSG_DETACHED_FLAG","CMSG_ENVELOPED","CMSG_HASHED","CMSG_SIGNED","CMSG_SIGNED_AND_ENVELOPED","CryptMsgOpenToEncode","CryptMsgOpenToEncode function [Security]","_crypto2_cryptmsgopentoencode","security.cryptmsgopentoencode","wincrypt/CryptMsgOpenToEncode"]
old-location: security\cryptmsgopentoencode.htm
tech.root: security
ms.assetid: b0d2610b-05ba-4fb6-8f38-10f970a52091
ms.date: 12/05/2018
ms.keywords: CMSG_AUTHENTICATED_ATTRIBUTES_FLAG, CMSG_BARE_CONTENT_FLAG, CMSG_CMS_ENCAPSULATED_CONTENT_FLAG, CMSG_CONTENTS_OCTETS_FLAG, CMSG_CRYPT_RELEASE_CONTEXT_FLAG, CMSG_DATA, CMSG_DETACHED_FLAG, CMSG_ENVELOPED, CMSG_HASHED, CMSG_SIGNED, CMSG_SIGNED_AND_ENVELOPED, CryptMsgOpenToEncode, CryptMsgOpenToEncode function [Security], _crypto2_cryptmsgopentoencode, security.cryptmsgopentoencode, wincrypt/CryptMsgOpenToEncode
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
 - CryptMsgOpenToEncode
 - wincrypt/CryptMsgOpenToEncode
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
 - CryptMsgOpenToEncode
---

# CryptMsgOpenToEncode function


## -description

The <b>CryptMsgOpenToEncode</b> function opens a cryptographic message for encoding and returns a handle of the opened message. The message remains open until 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> is called.

## -parameters

### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param dwFlags [in]

Currently defined <i>dwFlags</i> are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_BARE_CONTENT_FLAG"></a><a id="cmsg_bare_content_flag"></a><dl>
<dt><b>CMSG_BARE_CONTENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The streamed output will not have an outer ContentInfo wrapper (as defined by PKCS #7). This makes it suitable to be streamed into an enclosing message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_DETACHED_FLAG"></a><a id="cmsg_detached_flag"></a><dl>
<dt><b>CMSG_DETACHED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
There is detached data being supplied for the subsequent calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_AUTHENTICATED_ATTRIBUTES_FLAG"></a><a id="cmsg_authenticated_attributes_flag"></a><dl>
<dt><b>CMSG_AUTHENTICATED_ATTRIBUTES_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Authenticated attributes are forced to be included in the SignerInfo (as defined by PKCS #7) in cases where they would not otherwise be required.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENTS_OCTETS_FLAG"></a><a id="cmsg_contents_octets_flag"></a><dl>
<dt><b>CMSG_CONTENTS_OCTETS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Used when calculating the size of a message that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and that is nested inside an enveloped message. This is particularly useful when performing streaming.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_ENCAPSULATED_CONTENT_FLAG"></a><a id="cmsg_cms_encapsulated_content_flag"></a><dl>
<dt><b>CMSG_CMS_ENCAPSULATED_CONTENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When set, non-data type-<a href="/windows/desktop/SecGloss/i-gly">inner content</a> is encapsulated within an OCTET STRING. Applicable to both signed and enveloped messages.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CRYPT_RELEASE_CONTEXT_FLAG"></a><a id="cmsg_crypt_release_context_flag"></a><dl>
<dt><b>CMSG_CRYPT_RELEASE_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If set, the <b>hCryptProv</b> that is passed to this function is released on the final <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>. The handle is not released if the function fails.


<div class="alert"><b>Note</b>  The <b>hCryptProv</b>s of the envelope recipients are not released.</div>
<div> </div>
</td>
</tr>
</table>

### -param dwMsgType [in]

Indicates the message type. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_DATA"></a><a id="cmsg_data"></a><dl>
<dt><b>CMSG_DATA</b></dt>
</dl>
</td>
<td width="60%">
This value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED"></a><a id="cmsg_signed"></a><dl>
<dt><b>CMSG_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvMsgEncodeInfo</i> parameter is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure that contains the encoding information.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENVELOPED"></a><a id="cmsg_enveloped"></a><dl>
<dt><b>CMSG_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvMsgEncodeInfo</i> parameter is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure that contains the encoding information.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED_AND_ENVELOPED"></a><a id="cmsg_signed_and_enveloped"></a><dl>
<dt><b>CMSG_SIGNED_AND_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">
This value is not currently implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_HASHED"></a><a id="cmsg_hashed"></a><dl>
<dt><b>CMSG_HASHED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvMsgEncodeInfo</i> parameter is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_hashed_encode_info">CMSG_HASHED_ENCODE_INFO</a> structure that contains the encoding information.

</td>
</tr>
</table>

### -param pvMsgEncodeInfo [in]

The address of a structure that contains the encoding information. The type of data depends on the value of the <i>dwMsgType</i> parameter. For details, see <i>dwMsgType</i>.

### -param pszInnerContentObjID [in, optional]

If <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength">CryptMsgCalculateEncodedLength</a> is called and the data for 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a> has already been message encoded, the appropriate <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) is passed in <i>pszInnerContentObjID</i>. If <i>pszInnerContentObjID</i> is <b>NULL</b>, then the inner content type is assumed not to have been previously encoded and is therefore encoded as an octet string and given the type CMSG_DATA.

<div class="alert"><b>Note</b>  When streaming is being used, <i>pszInnerContentObjID</i> must be either <b>NULL</b> or szOID_RSA_data.</div>
<div> </div>
The following algorithm OIDs are commonly used. A user can define new inner content usage by ensuring that the sender and receiver of the message agree upon the semantics associated with the OID.

<ul>
<li>szOID_RSA_data</li>
<li>szOID_RSA_signedData</li>
<li>szOID_RSA_envelopedData</li>
<li>szOID_RSA_signEnvData</li>
<li>szOID_RSA_digestedData</li>
<li>szOID_RSA_encryptedData</li>
<li>SPC_INDIRECT_DATA_OBJID</li>
</ul>

### -param pStreamInfo [in]

When streaming is being used, this parameter is the address of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_stream_info">CMSG_STREAM_INFO</a> structure. The callback function specified by the <b>pfnStreamOutput</b> member of the <b>CMSG_STREAM_INFO</b> structure is called when 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a> is executed. The callback is passed the encoded bytes that result from the encoding. For more information about how to use the callback, see 
<b>CMSG_STREAM_INFO</b>.

<div class="alert"><b>Note</b>  When streaming is being used, the application must not release any data handles that are passed in the <i>pvMsgEncodeInfo</i> parameter, such as the provider handle in the <b>hCryptProv</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structure, until after the message handle returned by this function is closed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function.</div>
<div> </div>
When streaming is not being used, this parameter is set to <b>NULL</b>.

Streaming is not used with the <b>CMSG_HASHED</b> message type. When dealing with hashed data, this parameter must be set to <b>NULL</b>.

Consider the case of a signed message being enclosed in an enveloped message. The encoded output from the streamed encoding of the signed message feeds into another streaming encoding of the enveloped message. The callback for the streaming encoding calls <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a> to encode the enveloped message. The callback for the enveloped message receives the encoded bytes of the nested signed message.

## -returns

If the function succeeds, it returns a handle to the opened message. This handle must be closed when it is no longer needed by passing it to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function.

If this function fails, <b>NULL</b> is returned.

To retrieve extended error information, use the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The OID is badly formatted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory.

</td>
</tr>
</table>
 

In addition, if <i>dwMsgType</i> is CMSG_SIGNED, errors can be propagated from 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>.

If <i>dwMsgType</i> is CMSG_ENVELOPED, errors can be propagated from 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a>.

If <i>dwMsgType</i> is CMSG_HASHED, errors can be propagated from 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>.

## -remarks

For functions that perform encryption, the encrypted <a href="/windows/desktop/SecGloss/s-gly">symmetric keys</a> are reversed from <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> format to <a href="/windows/desktop/SecGloss/b-gly">big-endian</a> format after 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> is called internally. For functions that perform decryption, the encrypted symmetric keys are reversed from big-endian format to little-endian format before 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> is called.


CRYPT_NO_SALT is specified when symmetric keys are generated and imported with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>.

Messages encrypted with the RC2 encryption algorithm use KP_EFFECTIVE_KEYLEN with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> to determine the effective <a href="/windows/desktop/SecGloss/k-gly">key length</a> of the RC2 key importing or exporting keys.



For messages encrypted with the RC2 encryption algorithm, encode and decode operations have been updated to handle ASN RC2 parameters for the <b>ContentEncryptionAlgorithm</b> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure.



For messages encrypted with the RC4, DES, and 3DES encryption algorithms, encode and decode operations now handle the ASN IV octet string parameter for the <b>ContentEncryptionAlgorithm</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure.




#### Examples

For examples that use this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-signing-encoding-decoding-and-verifying-a-message">Example C Program: Signing, Encoding, Decoding, and Verifying a Message</a>, 
<a href="/windows/desktop/SecCrypto/alternate-code-for-encoding-an-enveloped-message">Alternate Code for Encoding an Enveloped Message</a>, 
<a href="/windows/desktop/SecCrypto/example-c-program-encoding-an-enveloped-signed-message">Example C Program: Encoding an Enveloped, Signed Message</a>, and 
<a href="/windows/desktop/SecCrypto/example-c-program-encoding-and-decoding-a-hashed-message">Example C Program: Encoding and Decoding a Hashed Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>