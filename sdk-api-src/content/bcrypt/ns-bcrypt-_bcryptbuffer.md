---
UID: NS:bcrypt._BCryptBuffer
title: "_BCryptBuffer"
author: windows-driver-content
description: Is used to represent a generic CNG buffer.
old-location: security\bcryptbuffer.htm
old-project: SecCNG
ms.assetid: abfc82f0-ec1c-41fb-8bf4-422a839d50c5
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PBCryptBuffer, BCryptBuffer, BCryptBuffer structure [Security], KDF_ALGORITHMID, KDF_CONTEXT, KDF_HASH_ALGORITHM, KDF_HMAC_KEY, KDF_ITERATION_COUNT, KDF_LABEL, KDF_PARTYUINFO, KDF_PARTYVINFO, KDF_SALT, KDF_SECRET_APPEND, KDF_SECRET_HANDLE, KDF_SECRET_PREPEND, KDF_SUPPPRIVINFO, KDF_SUPPPUBINFO, KDF_TLS_PRF_LABEL, KDF_TLS_PRF_PROTOCOL, KDF_TLS_PRF_SEED, PBCryptBuffer, PBCryptBuffer structure pointer [Security], _BCryptBuffer, bcrypt/BCryptBuffer, bcrypt/PBCryptBuffer, security.bcryptbuffer"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bcrypt.h
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
req.typenames: BCryptBuffer, *PBCryptBuffer
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	BCryptBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCryptBuffer structure


## -description


The <b>BCryptBuffer</b> structure is used to represent a generic CNG buffer.


## -struct-fields




### -field cbBuffer

The size, in bytes, of the buffer.


### -field BufferType

A value that specifies the type of buffer represented by this structure. This can be one of the following values.

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
The buffer is a KDF parameter that contains the value to add to the beginning of the message that is input to the hash function.

</td>
</tr>
<tr>
<td width="40%"><a id="KDF_SECRET_APPEND"></a><a id="kdf_secret_append"></a><dl>
<dt><b>KDF_SECRET_APPEND</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The buffer is a KDF parameter that contains the value to add to the end of the message that is input to the hash function.

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
<td width="40%"><a id="KDF_LABEL"></a><a id="kdf_label"></a><dl>
<dt><b>KDF_LABEL</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="KDF_CONTEXT"></a><a id="kdf_context"></a><dl>
<dt><b>KDF_CONTEXT</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="KDF_SALT"></a><a id="kdf_salt"></a><dl>
<dt><b>KDF_SALT</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="KDF_ITERATION_COUNT"></a><a id="kdf_iteration_count"></a><dl>
<dt><b>KDF_ITERATION_COUNT</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 


### -field pvBuffer

A 32-bit value defined by the <b>BufferType</b> member.


## -see-also




<a href="https://msdn.microsoft.com/7416d417-4b47-4830-aa20-a674d5270428">BCryptBufferDesc</a>



<a href="https://msdn.microsoft.com/33c3cbf7-6c08-42ed-ac3f-feb71f3a9cbf">BCryptDeriveKey</a>
 

 

