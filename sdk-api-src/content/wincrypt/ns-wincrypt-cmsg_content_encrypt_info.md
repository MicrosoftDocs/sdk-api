---
UID: NS:wincrypt._CMSG_CONTENT_ENCRYPT_INFO
title: CMSG_CONTENT_ENCRYPT_INFO (wincrypt.h)
description: Contains information shared between the PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY, PFN_CMSG_EXPORT_KEY_TRANS, PFN_CMSG_EXPORT_KEY_AGREE, and PFN_CMSG_EXPORT_MAIL_LIST functions.
helpviewer_keywords: ["*PCMSG_CONTENT_ENCRYPT_INFO","CMSG_CONTENT_ENCRYPT_FREE_OBJID_FLAG","CMSG_CONTENT_ENCRYPT_FREE_PARA_FLAG","CMSG_CONTENT_ENCRYPT_INFO","CMSG_CONTENT_ENCRYPT_INFO structure [Security]","CMSG_CONTENT_ENCRYPT_PAD_ENCODED_LEN_FLAG","CMSG_CONTENT_ENCRYPT_RELEASE_CONTEXT_FLAG","PCMSG_CONTENT_ENCRYPT_INFO","PCMSG_CONTENT_ENCRYPT_INFO structure pointer [Security]","RC2","RC4","security.cmsg_content_encrypt_info","wincrypt/CMSG_CONTENT_ENCRYPT_INFO","wincrypt/PCMSG_CONTENT_ENCRYPT_INFO"]
old-location: security\cmsg_content_encrypt_info.htm
tech.root: security
ms.assetid: c53014a0-049c-42ef-b612-8a1e03fb0dfd
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CONTENT_ENCRYPT_INFO, CMSG_CONTENT_ENCRYPT_FREE_OBJID_FLAG, CMSG_CONTENT_ENCRYPT_FREE_PARA_FLAG, CMSG_CONTENT_ENCRYPT_INFO, CMSG_CONTENT_ENCRYPT_INFO structure [Security], CMSG_CONTENT_ENCRYPT_PAD_ENCODED_LEN_FLAG, CMSG_CONTENT_ENCRYPT_RELEASE_CONTEXT_FLAG, PCMSG_CONTENT_ENCRYPT_INFO, PCMSG_CONTENT_ENCRYPT_INFO structure pointer [Security], RC2, RC4, security.cmsg_content_encrypt_info, wincrypt/CMSG_CONTENT_ENCRYPT_INFO, wincrypt/PCMSG_CONTENT_ENCRYPT_INFO'
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
req.typenames: CMSG_CONTENT_ENCRYPT_INFO, *PCMSG_CONTENT_ENCRYPT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CONTENT_ENCRYPT_INFO
 - wincrypt/_CMSG_CONTENT_ENCRYPT_INFO
 - PCMSG_CONTENT_ENCRYPT_INFO
 - wincrypt/PCMSG_CONTENT_ENCRYPT_INFO
 - CMSG_CONTENT_ENCRYPT_INFO
 - wincrypt/CMSG_CONTENT_ENCRYPT_INFO
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
 - CMSG_CONTENT_ENCRYPT_INFO
---

# CMSG_CONTENT_ENCRYPT_INFO structure


## -description

The <b>CMSG_CONTENT_ENCRYPT_INFO</b> structure contains information shared between the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key">PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY</a>, <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans">PFN_CMSG_EXPORT_KEY_TRANS</a>, <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree">PFN_CMSG_EXPORT_KEY_AGREE</a>, and <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list">PFN_CMSG_EXPORT_MAIL_LIST</a> functions used for the encryption and export of a content encryption key, which can be installed by using a Cryptography API: Next Generation (CNG) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hCryptProv

A handle to a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). If the <b>fCNG</b> member is <b>FALSE</b> and the <b>hCryptProv</b> member is <b>NULL</b> upon input, <b>hCryptProv</b> must be updated by the callback function. If a provider is acquired that must be released, the <b>CMSG_CONTENT_ENCRYPT_RELEASE_CONTEXT_FLAG</b> must be set in the <b>dwFlags</b> member.

### -field ContentEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to encrypt the key. If the callback function updates either the <b>pszObjId</b> member or the <b>Parameters</b> member of the <b>CRYPT_ALGORITHM_IDENTIFIER</b> structure, set the appropriate value in the <b>dwFlags</b> member. You must allocate and free memory for these values by using the <b>pfnAlloc</b> and <b>pfnFree</b> members.

### -field pvEncryptionAuxInfo

A pointer to a structure that depends on the encryption algorithm. The following table lists possible algorithm IDs and the corresponding member content.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RC2"></a><a id="rc2"></a><dl>
<dt><b>RC2</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="RC4"></a><a id="rc4"></a><dl>
<dt><b>RC4</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc4_aux_info">CMSG_RC4_AUX_INFO</a>


</td>
</tr>
</table>
 

For all other encryption algorithms, this value is <b>NULL</b>.

### -field cRecipients

A value that specifies the number of recipients of a message.

### -field rgCmsRecipients

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_recipient_encode_info">CMSG_RECIPIENT_ENCODE_INFO</a> structures that contain the message recipient information.

### -field pfnAlloc

A pointer to an installable function used to allocate memory for an updated member.

### -field pfnFree

A pointer to an installable function used to free memory allocated by <b>pfnAlloc</b>.

### -field dwEncryptFlags

A value that indicates whether the encoded output should be padded with zeros to obtain a consistent maximum length required for definite-length streaming in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength">CryptMsgCalculateEncodedLength</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> functions.



#### CMSG_CONTENT_ENCRYPT_PAD_ENCODED_LEN_FLAG (0x00000001)

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hContentEncryptKey

A handle to the content encryption key when the <b>fCNG</b> member is <b>FALSE</b>.

### -field DUMMYUNIONNAME.hCNGContentEncryptKey

A handle to the content encryption key when the <b>fCNG</b> member is <b>TRUE</b>.

### -field dwFlags

A value that indicates whether memory must be freed for the <b>hCryptProv</b> or <b>ContentEncryptionAlgorithm</b> members.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENT_ENCRYPT_FREE_PARA_FLAG"></a><a id="cmsg_content_encrypt_free_para_flag"></a><dl>
<dt><b>CMSG_CONTENT_ENCRYPT_FREE_PARA_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set if the callback function updates the <b>Parameters</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENT_ENCRYPT_FREE_OBJID_FLAG"></a><a id="cmsg_content_encrypt_free_objid_flag"></a><dl>
<dt><b>CMSG_CONTENT_ENCRYPT_FREE_OBJID_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Set if the callback function updates the <b>pszObjId</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENT_ENCRYPT_RELEASE_CONTEXT_FLAG"></a><a id="cmsg_content_encrypt_release_context_flag"></a><dl>
<dt><b>CMSG_CONTENT_ENCRYPT_RELEASE_CONTEXT_FLAG</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Set if the callback function acquires an <b>hCryptProv</b> member that must be freed.

</td>
</tr>
</table>

### -field fCNG

A value that indicates whether to use a <a href="/windows/desktop/SecGloss/c-gly">Cryptography API: Next Generation</a> (CNG) provider to generate the content encryption key.

If the <b>fCNG</b> member is <b>FALSE</b>, the <b>CMSG_OID_GEN_CONTENT_ENCRYPT_KEY_FUNC</b> function is called to update the <b>hContentEncryptKey</b> member.

If the <b>fCNG</b> member is <b>TRUE</b>, the  <b>CMSG_OID_CNG_GEN_CONTENT_ENCRYPT_KEY_FUNC</b> function is called to update the <b>hCNGContentEncryptKey</b> and <b>cbContentEncryptKey</b> members, and the <b>pbCNGContentEncryptKeyObject</b> and <b>pbContentEncryptKey</b> members must be allocated by the <b>pfnAlloc</b> member. Free and release the content encryption key by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function.

### -field pbCNGContentEncryptKeyObject

A pointer to the buffer that contains the CNG content encryption key.

### -field pbContentEncryptKey

A pointer to the buffer that contains a CAPI1 content encryption key.

### -field cbContentEncryptKey

The size, in bytes, of the <b>pbCNGContentEncryptKeyObject</b> or <b>pbContentEncryptKey</b> member depending on the value of the <b>fCNG</b> member.

## -remarks

When called with the <i>dwMsgType</i> parameter set to <b>CMSG_ENVELOPED</b>, the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function  initializes the <b>CMSG_CONTENT_ENCRYPT_INFO</b> structure from the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure.

If the  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure uses the <b>rgpRecipients</b> member instead of the <b>rgCmsRecipients</b> member, the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function converts the <b>rgpRecipients</b> member structures to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_recipient_encode_info">CMSG_RECIPIENT_ENCODE_INFO</a> structures for the <b>rgCmsRecipients</b> member of the <b>CMSG_CONTENT_ENCRYPT_INFO</b> structure.

When the <b>fCNG</b> member is <b>FALSE</b>, the following members can be changed in the <b>CMSG_CONTENT_ENCRYPT_INFO</b> structure:<dl>
<dd><b>hContentEncryptKey</b></dd>
<dd><b>hCryptProv</b></dd>
<dd>The <b>pszObjId</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member</dd>
<dd>The <b>Parameters</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member</dd>
<dd><b>dwFlags</b></dd>
</dl>


When the <b>fCNG</b> member is <b>TRUE</b>, the following members can be changed in the <b>CMSG_CONTENT_ENCRYPT_INFO</b> structure:<dl>
<dd><b>hCNGContentEncryptKey</b></dd>
<dd><b>pbCNGContentEncryptKeyObject</b></dd>
<dd><b>pbContentEncryptKey</b></dd>
<dd><b>cbContentEncryptKey</b></dd>
<dd>The <b>pszObjId</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member</dd>
<dd>The <b>Parameters</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure referred to by the <b>ContentEncryptionAlgorithm</b> member</dd>
<dd><b>dwFlags</b></dd>
</dl>


The following members are read-only:<dl>
<dd><b>cbSize</b></dd>
<dd><b>pvEncryptionAuxInfo</b></dd>
<dd><b>cRecipients</b></dd>
<dd><b>rgCmsRecipients</b></dd>
<dd><b>pfnAlloc</b></dd>
<dd><b>pfnFree</b></dd>
<dd><b>dwEncryptFlags</b></dd>
</dl>

## -see-also

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree">PFN_CMSG_EXPORT_KEY_AGREE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans">PFN_CMSG_EXPORT_KEY_TRANS</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list">PFN_CMSG_EXPORT_MAIL_LIST</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key">PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY</a>