---
UID: NS:wincrypt._CMSG_KEY_AGREE_ENCRYPT_INFO
title: CMSG_KEY_AGREE_ENCRYPT_INFO (wincrypt.h)
author: windows-sdk-content
description: Contains encryption information applicable to all key agreement recipients of an enveloped message.
old-location: security\cmsg_key_agree_encrypt_info.htm
tech.root: SecCrypto
ms.assetid: 7604ac82-a1a2-451b-8615-98303ce1d83e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCMSG_KEY_AGREE_ENCRYPT_INFO, CMSG_KEY_AGREE_ENCRYPT_FREE_MATERIAL_FLAG, CMSG_KEY_AGREE_ENCRYPT_FREE_OBJID_FLAG, CMSG_KEY_AGREE_ENCRYPT_FREE_PARA_FLAG, CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_ALG_FLAG, CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_BITS_FLAG, CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_PARA_FLAG, CMSG_KEY_AGREE_ENCRYPT_INFO, CMSG_KEY_AGREE_ENCRYPT_INFO structure [Security], CMSG_KEY_AGREE_ORIGINATOR_CERT, CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY, PCMSG_KEY_AGREE_ENCRYPT_INFO, PCMSG_KEY_AGREE_ENCRYPT_INFO structure pointer [Security], security.cmsg_key_agree_encrypt_info, wincrypt/CMSG_KEY_AGREE_ENCRYPT_INFO, wincrypt/PCMSG_KEY_AGREE_ENCRYPT_INFO"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_KEY_AGREE_ENCRYPT_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_KEY_AGREE_ENCRYPT_INFO, *PCMSG_KEY_AGREE_ENCRYPT_INFO
req.redist: 
ms.custom: 19H1
---

# CMSG_KEY_AGREE_ENCRYPT_INFO structure


## -description


The <b>CMSG_KEY_AGREE_ENCRYPT_INFO</b> structure contains encryption information applicable to all key agreement recipients of an enveloped message. The <a href="https://msdn.microsoft.com/5283f3be-7451-4896-82a5-bcfe63db9344">PFN_CMSG_EXPORT_KEY_AGREE</a> function updates this structure.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwRecipientIndex

A value that specifies the ordinal number of a recipient in the recipient list specified by the <i>pContentEncryptInfo</i> parameter of the <a href="https://msdn.microsoft.com/5283f3be-7451-4896-82a5-bcfe63db9344">PFN_CMSG_EXPORT_KEY_AGREE</a> function.


### -field KeyEncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to encrypt the content encryption key. The <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function uses the <b>pszObjId</b> member of the <b>CRYPT_ALGORITHM_IDENTIFIER</b> structure to get the address of the function used to export the key. The function can be installed by using a Cryptography API: Next Generation (CNG) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).


### -field UserKeyingMaterial

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains user keying material provided by the sender to ensure that a different key is generated each time the same two parties generate a pair-wise key.


### -field dwOriginatorChoice

A <b>DWORD</b> that indicates the key identifier to use. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ORIGINATOR_CERT"></a><a id="cmsg_key_agree_originator_cert"></a><dl>
<dt><b>CMSG_KEY_AGREE_ORIGINATOR_CERT</b></dt>
</dl>
</td>
<td width="60%">
OriginatorCertId

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY"></a><a id="cmsg_key_agree_originator_public_key"></a><dl>
<dt><b>CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY</b></dt>
</dl>
</td>
<td width="60%">
OriginatorPublicKeyInfo

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.OriginatorCertId

A <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure that identifies the public key of the message originator.


### -field DUMMYUNIONNAME.OriginatorPublicKeyInfo

A <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> of the message originator.


### -field cKeyAgreeKeyEncryptInfo

A value that specifies the number of recipients in the <i>rgpKeyAgreeKeyEncryptInfo</i> parameter.


### -field rgpKeyAgreeKeyEncryptInfo

An array of <a href="https://msdn.microsoft.com/586d40cc-8ef6-475b-8b7b-cc1a0bdddfcb">CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</a> structures that contain the encrypted key for each recipient.


### -field dwFlags

A value that specifies what members have been updated, and whose memory allocation must be freed by using the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_MATERIAL_FLAG"></a><a id="cmsg_key_agree_encrypt_free_material_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_MATERIAL_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>UserKeyingMaterial</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_OBJID_FLAG"></a><a id="cmsg_key_agree_encrypt_free_objid_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_OBJID_FLAG</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <b>pszObjId</b> member of the <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_PARA_FLAG"></a><a id="cmsg_key_agree_encrypt_free_para_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_PARA_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>Parameters</b> member of the <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_ALG_FLAG"></a><a id="cmsg_key_agree_encrypt_free_pubkey_alg_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_ALG_FLAG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <b>Algorithm.pszObjId</b> member of the <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure referred to by the <b>OriginatorPublicKeyInfo</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_BITS_FLAG"></a><a id="cmsg_key_agree_encrypt_free_pubkey_bits_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_BITS_FLAG</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The <b>PublicKey</b> member of the <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure referred to by the <b>OriginatorPublicKeyInfo</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_PARA_FLAG"></a><a id="cmsg_key_agree_encrypt_free_pubkey_para_flag"></a><dl>
<dt><b>CMSG_KEY_AGREE_ENCRYPT_FREE_PUBKEY_PARA_FLAG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <b>Algorithm.Parameters</b> member of the <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure referred to by the <b>OriginatorPublicKeyInfo</b> member was updated.

</td>
</tr>
</table>
 


## -remarks



 When called with the <i>dwMsgType</i> parameter set to <b>CMSG_ENVELOPED</b>, the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function initializes the <b>CMSG_KEY_AGREE_ENCRYPT_INFO</b> structure from the  <a href="https://msdn.microsoft.com/en-us/library/Aa377945(v=VS.85).aspx">CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</a> structure. The <b>CryptMsgOpenToEncode</b> function calls the <a href="https://msdn.microsoft.com/5283f3be-7451-4896-82a5-bcfe63db9344">PFN_CMSG_EXPORT_KEY_AGREE</a> function to update the <b>CMSG_KEY_AGREE_ENCRYPT_INFO</b> structure. If the callback function cannot be found, the <b>CryptMsgOpenToEncode</b> function fills this structure with default key information from the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure.

The following members of the <b>CMSG_KEY_AGREE_ENCRYPT_INFO</b> structure can be updated by the callback function:<dl>
<dd><b>UserKeyingMaterial</b></dd>
<dd><b>KeyEncryptionAlgorithm.pszObjId</b></dd>
<dd><b>KeyEncryptionAlgorithm.Parameters</b></dd>
<dd><b>dwOriginatorChoice</b></dd>
<dd><b>OriginatorCertId</b></dd>
<dd><b>OriginatorPublicKeyInfo</b></dd>
<dd><b>dwFlags</b></dd>
</dl>


The other members are read-only.



