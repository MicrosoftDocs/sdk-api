---
UID: NS:wincrypt._CMSG_KEY_TRANS_ENCRYPT_INFO
title: "_CMSG_KEY_TRANS_ENCRYPT_INFO"
author: windows-driver-content
description: Contains encryption information for a key transport recipient of enveloped data.
old-location: security\cmsg_key_trans_encrypt_info.htm
old-project: SecCrypto
ms.assetid: f3122acb-92c8-4803-8c74-8b3a2cf2e16e
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*PCMSG_KEY_TRANS_ENCRYPT_INFO, CMSG_KEY_TRANS_ENCRYPT_FREE_OBJID_FLAG, CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG, CMSG_KEY_TRANS_ENCRYPT_INFO, CMSG_KEY_TRANS_ENCRYPT_INFO structure [Security], PCMSG_KEY_TRANS_ENCRYPT_INFO, PCMSG_KEY_TRANS_ENCRYPT_INFO structure pointer [Security], _CMSG_KEY_TRANS_ENCRYPT_INFO, security.cmsg_key_trans_encrypt_info, wincrypt/CMSG_KEY_TRANS_ENCRYPT_INFO, wincrypt/PCMSG_KEY_TRANS_ENCRYPT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CMSG_KEY_TRANS_ENCRYPT_INFO, *PCMSG_KEY_TRANS_ENCRYPT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_KEY_TRANS_ENCRYPT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_KEY_TRANS_ENCRYPT_INFO structure


## -description


The <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure contains encryption information for a key transport recipient of enveloped data. The <a href="https://msdn.microsoft.com/bbb976df-5c8d-4d5e-ba92-7c534bba59de">PFN_CMSG_EXPORT_KEY_TRANS</a> function updates this structure.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwRecipientIndex

A value that specifies the ordinal number of a recipient in the recipient list specified by the <i>pContentEncryptInfo</i> parameter of the <a href="https://msdn.microsoft.com/bbb976df-5c8d-4d5e-ba92-7c534bba59de">PFN_CMSG_EXPORT_KEY_TRANS</a> function.


### -field KeyEncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm of the recipient public key. The <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function uses the <b>pszObjId</b> member of the <b>CRYPT_ALGORITHM_IDENTIFIER</b> structure to get the address of the function used to export the key. The function can be installed by using a Cryptography API: Next Generation (CNG) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the session key encrypted by the public key of the recipient.


### -field dwFlags

A value that specifies what members have been updated, and whose memory allocation must be freed by using the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_TRANS_ENCRYPT_FREE_OBJID_FLAG"></a><a id="cmsg_key_trans_encrypt_free_objid_flag"></a><dl>
<dt><b>CMSG_KEY_TRANS_ENCRYPT_FREE_OBJID_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>pszObjId</b> member of the <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG"></a><a id="cmsg_key_trans_encrypt_free_para_flag"></a><dl>
<dt><b>CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>Parameters</b> <b>pbData</b> member of the <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
</table>
 


## -remarks



 When called with the <i>dwMsgType</i> parameter set to <b>CMSG_ENVELOPED</b>, the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function initializes the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure from the  <a href="https://msdn.microsoft.com/20b20759-3d76-4814-9e71-7376dd326f7b">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure. The <b>CryptMsgOpenToEncode</b> function calls the <a href="https://msdn.microsoft.com/bbb976df-5c8d-4d5e-ba92-7c534bba59de">PFN_CMSG_EXPORT_KEY_TRANS</a> function to update the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure. If the callback function cannot be found, the <b>CryptMsgOpenToEncode</b> function fills this structure with default key information from the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure.

The following members of the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure can be updated by the callback function:<dl>
<dd><b>EncryptedKey</b></dd>
<dd><b>KeyEncryptionAlgorithm.pszObjId</b></dd>
<dd><b>KeyEncryptionAlgorithm.Parameters</b></dd>
<dd><b>dwFlags</b></dd>
</dl>


The other members are read-only.




## -see-also




<a href="https://msdn.microsoft.com/f35aacda-6827-42e9-b7ac-58dc007fc697">Encoding Enveloped Data</a>
 

 

