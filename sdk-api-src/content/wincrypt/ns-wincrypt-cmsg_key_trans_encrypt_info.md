---
UID: NS:wincrypt._CMSG_KEY_TRANS_ENCRYPT_INFO
title: CMSG_KEY_TRANS_ENCRYPT_INFO (wincrypt.h)
description: Contains encryption information for a key transport recipient of enveloped data.
helpviewer_keywords: ["*PCMSG_KEY_TRANS_ENCRYPT_INFO","CMSG_KEY_TRANS_ENCRYPT_FREE_OBJID_FLAG","CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG","CMSG_KEY_TRANS_ENCRYPT_INFO","CMSG_KEY_TRANS_ENCRYPT_INFO structure [Security]","PCMSG_KEY_TRANS_ENCRYPT_INFO","PCMSG_KEY_TRANS_ENCRYPT_INFO structure pointer [Security]","security.cmsg_key_trans_encrypt_info","wincrypt/CMSG_KEY_TRANS_ENCRYPT_INFO","wincrypt/PCMSG_KEY_TRANS_ENCRYPT_INFO"]
old-location: security\cmsg_key_trans_encrypt_info.htm
tech.root: security
ms.assetid: f3122acb-92c8-4803-8c74-8b3a2cf2e16e
ms.date: 12/05/2018
ms.keywords: '*PCMSG_KEY_TRANS_ENCRYPT_INFO, CMSG_KEY_TRANS_ENCRYPT_FREE_OBJID_FLAG, CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG, CMSG_KEY_TRANS_ENCRYPT_INFO, CMSG_KEY_TRANS_ENCRYPT_INFO structure [Security], PCMSG_KEY_TRANS_ENCRYPT_INFO, PCMSG_KEY_TRANS_ENCRYPT_INFO structure pointer [Security], security.cmsg_key_trans_encrypt_info, wincrypt/CMSG_KEY_TRANS_ENCRYPT_INFO, wincrypt/PCMSG_KEY_TRANS_ENCRYPT_INFO'
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
targetos: Windows
req.typenames: CMSG_KEY_TRANS_ENCRYPT_INFO, *PCMSG_KEY_TRANS_ENCRYPT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_KEY_TRANS_ENCRYPT_INFO
 - wincrypt/_CMSG_KEY_TRANS_ENCRYPT_INFO
 - PCMSG_KEY_TRANS_ENCRYPT_INFO
 - wincrypt/PCMSG_KEY_TRANS_ENCRYPT_INFO
 - CMSG_KEY_TRANS_ENCRYPT_INFO
 - wincrypt/CMSG_KEY_TRANS_ENCRYPT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_KEY_TRANS_ENCRYPT_INFO
---

# CMSG_KEY_TRANS_ENCRYPT_INFO structure


## -description

The <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure contains encryption information for a key transport recipient of enveloped data. The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans">PFN_CMSG_EXPORT_KEY_TRANS</a> function updates this structure.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwRecipientIndex

A value that specifies the ordinal number of a recipient in the recipient list specified by the <i>pContentEncryptInfo</i> parameter of the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans">PFN_CMSG_EXPORT_KEY_TRANS</a> function.

### -field KeyEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm of the recipient public key. The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function uses the <b>pszObjId</b> member of the <b>CRYPT_ALGORITHM_IDENTIFIER</b> structure to get the address of the function used to export the key. The function can be installed by using a Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

### -field EncryptedKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the session key encrypted by the public key of the recipient.

### -field dwFlags

A value that specifies what members have been updated, and whose memory allocation must be freed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function.

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
The <b>pszObjId</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG"></a><a id="cmsg_key_trans_encrypt_free_para_flag"></a><dl>
<dt><b>CMSG_KEY_TRANS_ENCRYPT_FREE_PARA_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>Parameters</b> <b>pbData</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>KeyEncryptionAlgorithm</b> member was updated.

</td>
</tr>
</table>

## -remarks

 When called with the <i>dwMsgType</i> parameter set to <b>CMSG_ENVELOPED</b>, the <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_encode_info">CryptMsgOpenToEncode</a> function initializes the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure from the  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_encode_info">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure. The <b>CryptMsgOpenToEncode</b> function calls the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans">PFN_CMSG_EXPORT_KEY_TRANS</a> function to update the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure. If the callback function cannot be found, the <b>CryptMsgOpenToEncode</b> function fills this structure with default key information from the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure.

The following members of the <b>CMSG_KEY_TRANS_ENCRYPT_INFO</b> structure can be updated by the callback function:<dl>
<dd><b>EncryptedKey</b></dd>
<dd><b>KeyEncryptionAlgorithm.pszObjId</b></dd>
<dd><b>KeyEncryptionAlgorithm.Parameters</b></dd>
<dd><b>dwFlags</b></dd>
</dl>


The other members are read-only.

## -see-also

<a href="/windows/desktop/SecCrypto/encoding-enveloped-data">Encoding Enveloped Data</a>