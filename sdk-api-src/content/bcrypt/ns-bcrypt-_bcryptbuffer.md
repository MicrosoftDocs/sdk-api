---
UID: NS:bcrypt._BCryptBuffer
title: "_BCryptBuffer"
author: windows-sdk-content
description: Is used to identify a variable-length memory buffer.
old-location: security\ncryptbuffer_struct.htm
old-project: seccng
ms.assetid: 474d3c0d-ae14-448a-a56d-25abc7e5de88
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PBCryptBuffer, BCryptBuffer, KDF_ALGORITHMID, KDF_HASH_ALGORITHM, KDF_HMAC_KEY, KDF_PARTYUINFO, KDF_PARTYVINFO, KDF_SECRET_APPEND, KDF_SECRET_HANDLE, KDF_SECRET_PREPEND, KDF_SUPPPRIVINFO, KDF_SUPPPUBINFO, KDF_TLS_PRF_LABEL, KDF_TLS_PRF_PROTOCOL, KDF_TLS_PRF_SEED, NCRYPTBUFFER_CERT_BLOB, NCRYPTBUFFER_PKCS_ALG_ID, NCRYPTBUFFER_PKCS_ALG_OID, NCRYPTBUFFER_PKCS_ALG_PARAM, NCRYPTBUFFER_PKCS_ATTRS, NCRYPTBUFFER_PKCS_KEY_NAME, NCRYPTBUFFER_PKCS_OID, NCRYPTBUFFER_PKCS_SECRET, NCRYPTBUFFER_SSL_CLEAR_KEY, NCRYPTBUFFER_SSL_CLIENT_RANDOM, NCRYPTBUFFER_SSL_HIGHEST_VERSION, NCRYPTBUFFER_SSL_KEY_ARG_DATA, NCRYPTBUFFER_SSL_SERVER_RANDOM, NCryptBuffer, NCryptBuffer structure [Security], PNCryptBuffer, PNCryptBuffer structure pointer [Security], _BCryptBuffer, bcrypt/NCryptBuffer, bcrypt/PNCryptBuffer, security.ncryptbuffer_struct"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BCryptBuffer, *PBCryptBuffer
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - NCryptBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCryptBuffer structure


## -description


The <b>NCryptBuffer</b> structure is used to identify a variable-length memory buffer.


## -struct-fields




### -field cbBuffer

The size, in bytes, of the buffer.


### -field BufferType

A value that identifies the type of data that is contained by the buffer. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KDF_HASH_ALGORITHM"></a><a id="kdf_hash_algorithm"></a><dl>
<dt><b>KDF_HASH_ALGORITHM</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The buffer is a key derivation function (KDF) parameter that contains a null-terminated Unicode string that identifies the hash algorithm. This can be one of the standard hash algorithm identifiers from <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or the identifier for another registered hash algorithm.

The size specified by the <b>cbBuffer</b> member of this structure must include the terminating <b>NULL</b> character.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SECRET_PREPEND"></a><a id="kdf_secret_prepend"></a><dl>
<dt><b>KDF_SECRET_PREPEND</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the value to add to the beginning of the message input to the hash function.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SECRET_APPEND"></a><a id="kdf_secret_append"></a><dl>
<dt><b>KDF_SECRET_APPEND</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the value to add to the end of the message input to the hash function.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_HMAC_KEY"></a><a id="kdf_hmac_key"></a><dl>
<dt><b>KDF_HMAC_KEY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the plain text value of the HMAC key.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_TLS_PRF_LABEL"></a><a id="kdf_tls_prf_label"></a><dl>
<dt><b>KDF_TLS_PRF_LABEL</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains an ANSI string that contains the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">transport layer security</a> (TLS) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">pseudo-random function</a> (PRF) label.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_TLS_PRF_SEED"></a><a id="kdf_tls_prf_seed"></a><dl>
<dt><b>KDF_TLS_PRF_SEED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the PRF seed value. The seed must be 64 bytes long.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SECRET_HANDLE"></a><a id="kdf_secret_handle"></a><dl>
<dt><b>KDF_SECRET_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the secret agreement handle. The <b>pvBuffer</b> member contains a <b>BCRYPT_SECRET_HANDLE</b> value and is not a pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_TLS_PRF_PROTOCOL"></a><a id="kdf_tls_prf_protocol"></a><dl>
<dt><b>KDF_TLS_PRF_PROTOCOL</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains a DWORD value identifying the SSL/TLS protocol version whose PRF algorithm is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_ALGORITHMID"></a><a id="kdf_algorithmid"></a><dl>
<dt><b>KDF_ALGORITHMID</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the byte array to use as the <b>AlgorithmID</b> subfield of the <i>OtherInfo</i> parameter to the SP 800-56A KDF.


</td>
</tr>
<tr>
<td width="40%"><a id="KDF_PARTYUINFO"></a><a id="kdf_partyuinfo"></a><dl>
<dt><b>KDF_PARTYUINFO</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the byte array to use as the <b>PartyUInfo</b> subfield of the <i>OtherInfo</i> parameter to the SP 800-56A KDF.


</td>
</tr>
<tr>
<td width="40%"><a id="KDF_PARTYVINFO"></a><a id="kdf_partyvinfo"></a><dl>
<dt><b>KDF_PARTYVINFO</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the byte array to use as the <b>PartyVInfo</b> subfield of the <i>OtherInfo</i> parameter to the SP 800-56A KDF.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SUPPPUBINFO"></a><a id="kdf_supppubinfo"></a><dl>
<dt><b>KDF_SUPPPUBINFO</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the byte array to use as the <b>SuppPubInfo</b> subfield of the <i>OtherInfo</i> parameter to the SP 800-56A KDF.


</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SUPPPRIVINFO"></a><a id="kdf_suppprivinfo"></a><dl>
<dt><b>KDF_SUPPPRIVINFO</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the byte array to use as the <b>SuppPrivInfo</b> subfield of the <i>OtherInfo</i> parameter to the SP 800-56A KDF.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_SSL_CLIENT_RANDOM"></a><a id="ncryptbuffer_ssl_client_random"></a><dl>
<dt><b>NCRYPTBUFFER_SSL_CLIENT_RANDOM</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
The buffer contains the random number of the SSL client.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_SSL_SERVER_RANDOM"></a><a id="ncryptbuffer_ssl_server_random"></a><dl>
<dt><b>NCRYPTBUFFER_SSL_SERVER_RANDOM</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
The buffer contains the random number of the SSL server.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_SSL_HIGHEST_VERSION"></a><a id="ncryptbuffer_ssl_highest_version"></a><dl>
<dt><b>NCRYPTBUFFER_SSL_HIGHEST_VERSION</b></dt>
<dt>22</dt>
</dl>
</td>
<td width="60%">
The buffer contains the highest SSL version supported.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_SSL_CLEAR_KEY"></a><a id="ncryptbuffer_ssl_clear_key"></a><dl>
<dt><b>NCRYPTBUFFER_SSL_CLEAR_KEY</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The buffer contains the clear portion of the SSL master key.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_SSL_KEY_ARG_DATA"></a><a id="ncryptbuffer_ssl_key_arg_data"></a><dl>
<dt><b>NCRYPTBUFFER_SSL_KEY_ARG_DATA</b></dt>
<dt>24</dt>
</dl>
</td>
<td width="60%">
The buffer contains the SSL key argument data.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_OID"></a><a id="ncryptbuffer_pkcs_oid"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_OID</b></dt>
<dt>40</dt>
</dl>
</td>
<td width="60%">
The buffer contains a null-terminated ANSI string that contains the PKCS object identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_ALG_OID"></a><a id="ncryptbuffer_pkcs_alg_oid"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_ALG_OID</b></dt>
<dt>41</dt>
</dl>
</td>
<td width="60%">
The buffer contains a null-terminated ANSI string that contains the PKCS algorithm object identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_ALG_PARAM"></a><a id="ncryptbuffer_pkcs_alg_param"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_ALG_PARAM</b></dt>
<dt>42</dt>
</dl>
</td>
<td width="60%">
The buffer contains the PKCS algorithm parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_ALG_ID"></a><a id="ncryptbuffer_pkcs_alg_id"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_ALG_ID</b></dt>
<dt>43</dt>
</dl>
</td>
<td width="60%">
The buffer contains the PKCS algorithm identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_ATTRS"></a><a id="ncryptbuffer_pkcs_attrs"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_ATTRS</b></dt>
<dt>44</dt>
</dl>
</td>
<td width="60%">
The buffer contains the PKCS attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_KEY_NAME"></a><a id="ncryptbuffer_pkcs_key_name"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_KEY_NAME</b></dt>
<dt>45</dt>
</dl>
</td>
<td width="60%">
The buffer contains a null-terminated Unicode string that contains the key name.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_PKCS_SECRET"></a><a id="ncryptbuffer_pkcs_secret"></a><dl>
<dt><b>NCRYPTBUFFER_PKCS_SECRET</b></dt>
<dt>46</dt>
</dl>
</td>
<td width="60%">
The buffer contains a null-terminated Unicode string that contains the PKCS8 password. This parameter is optional and can be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPTBUFFER_CERT_BLOB"></a><a id="ncryptbuffer_cert_blob"></a><dl>
<dt><b>NCRYPTBUFFER_CERT_BLOB</b></dt>
<dt>47</dt>
</dl>
</td>
<td width="60%">
The buffer contains a serialized certificate store that contains the PKCS certificate. This serialized store is obtained by using the <a href="https://msdn.microsoft.com/5cc818d7-b079-4962-aabc-fc512d4e92ac">CertSaveStore</a> function with the <b>CERT_STORE_SAVE_TO_MEMORY</b> option. When this property is being retrieved, you can access the certificate store by passing this serialized store to the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function with the <b>CERT_STORE_PROV_SERIALIZED</b> option.

</td>
</tr>
</table>
 


### -field pvBuffer

The address of the buffer. The size of this buffer is contained in the <b>cbBuffer</b> member.

The format and contents of this buffer are identified by the <b>BufferType</b> member.


## -remarks



BCryptBuffer is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/ae4673ab-81cd-4604-bafa-8d8c66003aba">NCryptBufferDesc</a>



<a href="https://msdn.microsoft.com/1588eb29-4026-4d1c-8bee-a035df38444a">NCryptExportKey</a>
 

 

