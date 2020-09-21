---
UID: NF:wincrypt.CryptMsgGetParam
title: CryptMsgGetParam function (wincrypt.h)
description: Acquires a message parameter after a cryptographic message has been encoded or decoded.
helpviewer_keywords: ["CMSG_ATTR_CERT_COUNT_PARAM","CMSG_ATTR_CERT_PARAM","CMSG_BARE_CONTENT_PARAM","CMSG_CERT_COUNT_PARAM","CMSG_CERT_PARAM","CMSG_CMS_RECIPIENT_COUNT_PARAM","CMSG_CMS_RECIPIENT_ENCRYPTED_KEY_INDEX_PARAM","CMSG_CMS_RECIPIENT_INDEX_PARAM","CMSG_CMS_RECIPIENT_INFO_PARAM","CMSG_CMS_SIGNER_INFO_PARAM","CMSG_COMPUTED_HASH_PARAM","CMSG_CONTENT_PARAM","CMSG_CRL_COUNT_PARAM","CMSG_CRL_PARAM","CMSG_ENCODED_MESSAGE","CMSG_ENCODED_SIGNER","CMSG_ENCRYPTED_DIGEST","CMSG_ENCRYPT_PARAM","CMSG_ENVELOPE_ALGORITHM_PARAM","CMSG_HASH_ALGORITHM_PARAM","CMSG_HASH_DATA_PARAM","CMSG_INNER_CONTENT_TYPE_PARAM","CMSG_RECIPIENT_COUNT_PARAM","CMSG_RECIPIENT_INDEX_PARAM","CMSG_RECIPIENT_INFO_PARAM","CMSG_SIGNER_AUTH_ATTR_PARAM","CMSG_SIGNER_CERT_ID_PARAM","CMSG_SIGNER_CERT_INFO_PARAM","CMSG_SIGNER_COUNT_PARAM","CMSG_SIGNER_HASH_ALGORITHM_PARAM","CMSG_SIGNER_INFO_PARAM","CMSG_SIGNER_UNAUTH_ATTR_PARAM","CMSG_TYPE_PARAM","CMSG_UNPROTECTED_ATTR_PARAM","CMSG_VERSION_PARAM","CryptMsgGetParam","CryptMsgGetParam function [Security]","_crypto2_cryptmsggetparam","security.cryptmsggetparam","wincrypt/CryptMsgGetParam"]
old-location: security\cryptmsggetparam.htm
tech.root: security
ms.assetid: 5a05eb09-208f-4e94-abfa-c2f14c0a3164
ms.date: 12/05/2018
ms.keywords: CMSG_ATTR_CERT_COUNT_PARAM, CMSG_ATTR_CERT_PARAM, CMSG_BARE_CONTENT_PARAM, CMSG_CERT_COUNT_PARAM, CMSG_CERT_PARAM, CMSG_CMS_RECIPIENT_COUNT_PARAM, CMSG_CMS_RECIPIENT_ENCRYPTED_KEY_INDEX_PARAM, CMSG_CMS_RECIPIENT_INDEX_PARAM, CMSG_CMS_RECIPIENT_INFO_PARAM, CMSG_CMS_SIGNER_INFO_PARAM, CMSG_COMPUTED_HASH_PARAM, CMSG_CONTENT_PARAM, CMSG_CRL_COUNT_PARAM, CMSG_CRL_PARAM, CMSG_ENCODED_MESSAGE, CMSG_ENCODED_SIGNER, CMSG_ENCRYPTED_DIGEST, CMSG_ENCRYPT_PARAM, CMSG_ENVELOPE_ALGORITHM_PARAM, CMSG_HASH_ALGORITHM_PARAM, CMSG_HASH_DATA_PARAM, CMSG_INNER_CONTENT_TYPE_PARAM, CMSG_RECIPIENT_COUNT_PARAM, CMSG_RECIPIENT_INDEX_PARAM, CMSG_RECIPIENT_INFO_PARAM, CMSG_SIGNER_AUTH_ATTR_PARAM, CMSG_SIGNER_CERT_ID_PARAM, CMSG_SIGNER_CERT_INFO_PARAM, CMSG_SIGNER_COUNT_PARAM, CMSG_SIGNER_HASH_ALGORITHM_PARAM, CMSG_SIGNER_INFO_PARAM, CMSG_SIGNER_UNAUTH_ATTR_PARAM, CMSG_TYPE_PARAM, CMSG_UNPROTECTED_ATTR_PARAM, CMSG_VERSION_PARAM, CryptMsgGetParam, CryptMsgGetParam function [Security], _crypto2_cryptmsggetparam, security.cryptmsggetparam, wincrypt/CryptMsgGetParam
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
 - CryptMsgGetParam
 - wincrypt/CryptMsgGetParam
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
 - CryptMsgGetParam
---

# CryptMsgGetParam function


## -description

The <b>CryptMsgGetParam</b> function acquires a message parameter after a cryptographic message has been encoded or decoded. This function is called after the final 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a> call.

## -parameters

### -param hCryptMsg [in]

Handle of a cryptographic message.

### -param dwParamType [in]

Indicates the parameter types of data to be retrieved. The type of data to be retrieved determines the type of structure to use for <i>pvData</i>. 




For an encoded message, only the CMSG_BARE_CONTENT, CMSG_ENCODE_SIGNER, CMSG_CONTENT_PARAM and CMSG_COMPUTED_HASH_PARAM <i>dwParamType</i>s are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_ATTR_CERT_COUNT_PARAM"></a><a id="cmsg_attr_cert_count_param"></a><dl>
<dt><b>CMSG_ATTR_CERT_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

 Returns the count of the attribute certificates in a SIGNED or ENVELOPED message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ATTR_CERT_PARAM"></a><a id="cmsg_attr_cert_param"></a><dl>
<dt><b>CMSG_ATTR_CERT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Retrieves an attribute certificate. To get all the attribute certificates, call <b>CryptMsgGetParam</b> varying <i>dwIndex</i> set to 0 the number of attributes minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_BARE_CONTENT_PARAM"></a><a id="cmsg_bare_content_param"></a><dl>
<dt><b>CMSG_BARE_CONTENT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Retrieves the encoded content of an encoded cryptographic message, without the outer layer of the CONTENT_INFO structure. That is, only the encoding of the PKCS #7 defined ContentInfo.content field is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CERT_COUNT_PARAM"></a><a id="cmsg_cert_count_param"></a><dl>
<dt><b>CMSG_CERT_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to <b>DWORD</b>

Returns the number of certificates in a received SIGNED or ENVELOPED message.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CERT_PARAM"></a><a id="cmsg_cert_param"></a><dl>
<dt><b>CMSG_CERT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns a signer's certificate. To get all of the signer's certificates, call <b>CryptMsgGetParam</b>, varying <i>dwIndex</i> from 0 to the number of available certificates minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_COMPUTED_HASH_PARAM"></a><a id="cmsg_computed_hash_param"></a><dl>
<dt><b>CMSG_COMPUTED_HASH_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns the  hash calculated of the data in the message. This type is applicable to both encode and decode.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENT_PARAM"></a><a id="cmsg_content_param"></a><dl>
<dt><b>CMSG_CONTENT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

 


Returns the whole PKCS #7 message from a message opened to encode. Retrieves the inner content of a message opened to decode. If the message is enveloped, the inner type is data, and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> has been called to decrypt the message, the decrypted content is returned. If the inner type is not data, the encoded BLOB that requires further decoding is returned.
If the message is not enveloped and the inner content is DATA, the returned data is the octets of the inner content.
This type is applicable to both encode and decode.

For decoding, if the type is CMSG_DATA, the content's octets are returned; else, the encoded inner content is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CRL_COUNT_PARAM"></a><a id="cmsg_crl_count_param"></a><dl>
<dt><b>CMSG_CRL_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to <b>DWORD</b>

Returns the count of CRLs in a received, SIGNED or ENVELOPED message.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CRL_PARAM"></a><a id="cmsg_crl_param"></a><dl>
<dt><b>CMSG_CRL_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns a CRL. To get all the CRLs, call <b>CryptMsgGetParam</b>, varying <i>dwIndex</i> from 0 to the number of available CRLs minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENCODED_MESSAGE"></a><a id="cmsg_encoded_message"></a><dl>
<dt><b>CMSG_ENCODED_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Changes the contents of an already encoded message. The message must first be decoded with a call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>. Then the change to the message is made through a call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersign">CryptMsgCountersign</a>, or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersignencoded">CryptMsgCountersignEncoded</a>. The message is then encoded again with a call to <b>CryptMsgGetParam</b>, specifying CMSG_ENCODED_MESSAGE to get a new encoding that reflects the changes made. This can be used, for instance, to add a time-stamp attribute to a message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENCODED_SIGNER"></a><a id="cmsg_encoded_signer"></a><dl>
<dt><b>CMSG_ENCODED_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns the encoded CMSG_SIGNER_INFO signer information for a message signer.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENCRYPTED_DIGEST"></a><a id="cmsg_encrypted_digest"></a><dl>
<dt><b>CMSG_ENCRYPTED_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns the encrypted hash of a signature. Typically used for performing time-stamping.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENCRYPT_PARAM"></a><a id="cmsg_encrypt_param"></a><dl>
<dt><b>CMSG_ENCRYPT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array for a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure.

 Returns the encryption algorithm used to encrypted the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENVELOPE_ALGORITHM_PARAM"></a><a id="cmsg_envelope_algorithm_param"></a><dl>
<dt><b>CMSG_ENVELOPE_ALGORITHM_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array for a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure.

 Returns the encryption algorithm used to encrypt an ENVELOPED message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_HASH_ALGORITHM_PARAM"></a><a id="cmsg_hash_algorithm_param"></a><dl>
<dt><b>CMSG_HASH_ALGORITHM_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array for a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure.

 Returns the hash algorithm used to hash the message when it was created.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_HASH_DATA_PARAM"></a><a id="cmsg_hash_data_param"></a><dl>
<dt><b>CMSG_HASH_DATA_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array

Returns the hash value stored in the message when it was created.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_INNER_CONTENT_TYPE_PARAM"></a><a id="cmsg_inner_content_type_param"></a><dl>
<dt><b>CMSG_INNER_CONTENT_TYPE_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a <b>null</b>-terminated <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string.

Returns the inner content type of a received message. This type is not applicable to messages of type DATA.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_RECIPIENT_COUNT_PARAM"></a><a id="cmsg_recipient_count_param"></a><dl>
<dt><b>CMSG_RECIPIENT_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the number of key transport recipients of an ENVELOPED received message.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_RECIPIENT_COUNT_PARAM"></a><a id="cmsg_cms_recipient_count_param"></a><dl>
<dt><b>CMSG_CMS_RECIPIENT_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to <b>DWORD</b>

Returns the total count of all message recipients including key agreement and mail list recipients.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_RECIPIENT_INDEX_PARAM"></a><a id="cmsg_recipient_index_param"></a><dl>
<dt><b>CMSG_RECIPIENT_INDEX_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the index of the key transport recipient used to decrypt an ENVELOPED message. This value is available only after a message has been decrypted.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_RECIPIENT_INDEX_PARAM"></a><a id="cmsg_cms_recipient_index_param"></a><dl>
<dt><b>CMSG_CMS_RECIPIENT_INDEX_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the index of the key transport, key agreement, or mail list recipient used to decrypt an ENVELOPED message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_RECIPIENT_ENCRYPTED_KEY_INDEX_PARAM"></a><a id="cmsg_cms_recipient_encrypted_key_index_param"></a><dl>
<dt><b>CMSG_CMS_RECIPIENT_ENCRYPTED_KEY_INDEX_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the index of the encrypted key of a key agreement recipient used to decrypt an ENVELOPED message.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_RECIPIENT_INFO_PARAM"></a><a id="cmsg_recipient_info_param"></a><dl>
<dt><b>CMSG_RECIPIENT_INFO_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

 Returns certificate information about a key transport message's recipient. To get certificate information on all key transport message's recipients, repetitively call <b>CryptMsgGetParam</b>, varying <i>dwIndex</i> from 0 to the number of recipients minus one.
Only the Issuer, SerialNumber, and PublicKeyAlgorithm members of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure returned are available and valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_RECIPIENT_INFO_PARAM"></a><a id="cmsg_cms_recipient_info_param"></a><dl>
<dt><b>CMSG_CMS_RECIPIENT_INFO_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_cms_recipient_info">CMSG_CMS_RECIPIENT_INFO</a> structure.

Returns information about a key transport, key agreement, or mail list recipient. It is not limited to key transport message recipients.
To get information on all of a message's recipients, repetitively call <b>CryptMsgGetParam</b>, varying <i>dwIndex</i> from 0 to the number of recipients minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_AUTH_ATTR_PARAM"></a><a id="cmsg_signer_auth_attr_param"></a><dl>
<dt><b>CMSG_SIGNER_AUTH_ATTR_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure.

 Returns the authenticated attributes of a message signer. To retrieve the authenticated attributes for a specified signer, call <b>CryptMsgGetParam</b> with <i>dwIndex</i> equal to that signer's index.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_CERT_INFO_PARAM"></a><a id="cmsg_signer_cert_info_param"></a><dl>
<dt><b>CMSG_SIGNER_CERT_INFO_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

 Returns information on a message signer needed to identify the signer's certificate. A certificate's Issuer and SerialNumber can be used to uniquely identify a certificate for retrieval. To retrieve information for all the signers, repetitively call <b>CryptMsgGetParam</b> varying <i>dwIndex</i> from 0 to the number of signers minus one.
Only the Issuer and SerialNumber fields in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure returned contain available, valid data.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_CERT_ID_PARAM"></a><a id="cmsg_signer_cert_id_param"></a><dl>
<dt><b>CMSG_SIGNER_CERT_ID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure.

Returns information on a message signer needed to identify the signer's public key. This could be a certificate's Issuer and SerialNumber, a KeyID, or a HashId. To retrieve information for all the signers, call <b>CryptMsgGetParam</b> varying <i>dwIndex</i> from 0 to the number of signers minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_COUNT_PARAM"></a><a id="cmsg_signer_count_param"></a><dl>
<dt><b>CMSG_SIGNER_COUNT_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the number of signers of a received SIGNED message.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_HASH_ALGORITHM_PARAM"></a><a id="cmsg_signer_hash_algorithm_param"></a><dl>
<dt><b>CMSG_SIGNER_HASH_ALGORITHM_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure.

 Returns the hash algorithm used by a signer of the message. To get the hash algorithm for a specified signer, call <b>CryptMsgGetParam</b> with <i>dwIndex</i> equal to that signer's index.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_INFO_PARAM"></a><a id="cmsg_signer_info_param"></a><dl>
<dt><b>CMSG_SIGNER_INFO_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a> structure.

 Returns information on a message signer. This includes the issuer and serial number of the signer's certificate and authenticated and unauthenticated attributes of the signer's certificate.
To retrieve signer information on all of the signers of a message, call <b>CryptMsgGetParam</b> varying <i>dwIndex</i> from 0 to the number of signers minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_SIGNER_INFO_PARAM"></a><a id="cmsg_cms_signer_info_param"></a><dl>
<dt><b>CMSG_CMS_SIGNER_INFO_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_cms_signer_info">CMSG_CMS_SIGNER_INFO</a> structure.

 Returns information on a message signer. This includes a signerId and authenticated and unauthenticated attributes.
To retrieve signer information on all of the signers of a message, call <b>CryptMsgGetParam</b> varying <i>dwIndex</i> from 0 to the number of signers minus one.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_UNAUTH_ATTR_PARAM"></a><a id="cmsg_signer_unauth_attr_param"></a><dl>
<dt><b>CMSG_SIGNER_UNAUTH_ATTR_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure.

 Returns a message signer's unauthenticated attributes. To retrieve the unauthenticated attributes for a specified signer, call <b>CryptMsgGetParam</b>  with <i>dwIndex</i> equal to that signer's index.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_TYPE_PARAM"></a><a id="cmsg_type_param"></a><dl>
<dt><b>CMSG_TYPE_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

Returns the message type of a decoded message of unknown type. The retrieved message type can be compared to supported types to determine whether processing can continued. For supported message types, see the <i>dwMessageType</i> parameter of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_UNPROTECTED_ATTR_PARAM"></a><a id="cmsg_unprotected_attr_param"></a><dl>
<dt><b>CMSG_UNPROTECTED_ATTR_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>BYTE</b> array to receive a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CMSG_ATTR</a> structure.

 Returns the unprotected attributes in an enveloped message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_VERSION_PARAM"></a><a id="cmsg_version_param"></a><dl>
<dt><b>CMSG_VERSION_PARAM</b></dt>
</dl>
</td>
<td width="60%">
<i>pvData</i> data type: pointer to a <b>DWORD</b>

 Returns the version of the decoded message. For more information, see the table in the Remarks section.

</td>
</tr>
</table>

### -param dwIndex [in]

Index for the parameter being retrieved, where applicable. When a parameter is not being retrieved, this parameter is ignored and is set to zero.

### -param pvData [out]

A pointer to a buffer that receives the data retrieved. The form of this data will vary depending on the value of the <i>dwParamType</i> parameter. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

When processing the data returned in this buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.

### -param pcbData [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, the variable pointed to by the <i>pcbData</i> parameter contains the number of bytes stored in the buffer.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_ATTRIBUTES_MISSING</b></dt>
</dl>
</td>
<td width="60%">
The message does not contain the requested attributes.

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
<dt><b>CRYPT_E_NOT_DECRYPTED</b></dt>
</dl>
</td>
<td width="60%">
The message content has not been decrypted yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_OID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The object identifier is badly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified buffer is not large enough to hold the returned data.

</td>
</tr>
</table>
 

For <i>dwParamType</i> CMSG_COMPUTED_HASH_PARAM, an error can be propagated from 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>.

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

The following version numbers are returned by calls to <b>CryptMsgGetParam</b> with <i>dwParamType</i> set to CMSG_VERSION_PARAM are defined:

<ul>
<li>CMSG_SIGNED_DATA_V1</li>
<li>CMSG_SIGNED_DATA_V3</li>
<li>CMSG_SIGNED_DATA_PKCS_1_5_VERSION</li>
<li>CMSG_SIGNED_DATA_CMS_VERSION</li>
<li>CMSG_SIGNER_INFO_V1</li>
<li>CMSG_SIGNER_INFO_V3</li>
<li>CMSG_SIGNER_INFO_PKCS_1_5_VERSION</li>
<li>CMSG_SIGNER_INFO_CMS_VERSION</li>
<li>CMSG_HASHED_DATA_V0</li>
<li>CMSG_HASHED_DATA_V2</li>
<li>CMSG_HASHED_DATA_PKCS_1_5_VERSION</li>
<li>CMSG_HASHED_DATA_CMS_VERSION</li>
<li>CMSG_ENVELOPED_DATA_V0</li>
<li>CMSG_ENVELOPED_DATA_V2</li>
<li>CMSG_ENVELOPED_DATA_PKCS_1_5_VERSION</li>
<li>CMSG_ENVELOPED_DATA_CMS_VERSION</li>
</ul>

#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-signing-encoding-decoding-and-verifying-a-message">Example C Program: Signing, Encoding, Decoding, and Verifying a Message</a>, 
<a href="/windows/desktop/SecCrypto/alternate-code-for-encoding-an-enveloped-message">Alternate Code for Encoding an Enveloped Message</a>, 
<a href="/windows/desktop/SecCrypto/example-c-program-encoding-an-enveloped-signed-message">Example C Program: Encoding an Enveloped, Signed Message</a>, and 
<a href="/windows/desktop/SecCrypto/example-c-program-encoding-and-decoding-a-hashed-message">Example C Program: Encoding and Decoding a Hashed Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>