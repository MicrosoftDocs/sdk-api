---
UID: NS:wincrypt._CMSG_CMS_RECIPIENT_INFO
title: CMSG_CMS_RECIPIENT_INFO (wincrypt.h)
description: Used with the CryptMsgGetParam function to get information on a key transport, key agreement, or mail list envelope message recipient.
helpviewer_keywords: ["*PCMSG_CMS_RECIPIENT_INFO","CMSG_CMS_RECIPIENT_INFO","CMSG_CMS_RECIPIENT_INFO structure [Security]","CMSG_KEY_AGREE_RECIPIENT","CMSG_KEY_TRANS_RECIPIENT","CMSG_MAIL_LIST_RECIPIENT","PCMSG_CMS_RECIPIENT_INFO","PCMSG_CMS_RECIPIENT_INFO structure pointer [Security]","_crypto2_cmsg_cms_recipient_info","security.cmsg_cms_recipient_info","wincrypt/CMSG_CMS_RECIPIENT_INFO","wincrypt/PCMSG_CMS_RECIPIENT_INFO"]
old-location: security\cmsg_cms_recipient_info.htm
tech.root: security
ms.assetid: 27ce2430-d240-49f7-bff7-32be1695c8c0
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CMS_RECIPIENT_INFO, CMSG_CMS_RECIPIENT_INFO, CMSG_CMS_RECIPIENT_INFO structure [Security], CMSG_KEY_AGREE_RECIPIENT, CMSG_KEY_TRANS_RECIPIENT, CMSG_MAIL_LIST_RECIPIENT, PCMSG_CMS_RECIPIENT_INFO, PCMSG_CMS_RECIPIENT_INFO structure pointer [Security], _crypto2_cmsg_cms_recipient_info, security.cmsg_cms_recipient_info, wincrypt/CMSG_CMS_RECIPIENT_INFO, wincrypt/PCMSG_CMS_RECIPIENT_INFO'
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
req.typenames: CMSG_CMS_RECIPIENT_INFO, *PCMSG_CMS_RECIPIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CMS_RECIPIENT_INFO
 - wincrypt/_CMSG_CMS_RECIPIENT_INFO
 - PCMSG_CMS_RECIPIENT_INFO
 - wincrypt/PCMSG_CMS_RECIPIENT_INFO
 - CMSG_CMS_RECIPIENT_INFO
 - wincrypt/CMSG_CMS_RECIPIENT_INFO
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
 - CMSG_CMS_RECIPIENT_INFO
---

# CMSG_CMS_RECIPIENT_INFO structure


## -description

The <b>CMSG_CMS_RECIPIENT_INFO</b> structure is used with the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> function to get information on a key transport, key agreement, or mail list envelope message recipient. This structure is returned in <i>pvData</i> when <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> is called with <i>dwParamType</i> set to CMSG_CMS_RECIPIENT_INFO_PARAM.

## -struct-fields

### -field dwRecipientChoice

Indicates the member of the union to be used. 




Possible values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_TRANS_RECIPIENT"></a><a id="cmsg_key_trans_recipient"></a><dl>
<dt><b>CMSG_KEY_TRANS_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
pKeyTrans

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_RECIPIENT"></a><a id="cmsg_key_agree_recipient"></a><dl>
<dt><b>CMSG_KEY_AGREE_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
pKeyAgree

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_MAIL_LIST_RECIPIENT"></a><a id="cmsg_mail_list_recipient"></a><dl>
<dt><b>CMSG_MAIL_LIST_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
pMailList

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pKeyTrans

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_info">CMSG_KEY_TRANS_RECIPIENT_INFO</a> structure that identifies a key transport recipient. Used for RSA recipients.

### -field DUMMYUNIONNAME.pKeyAgree

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_recipient_info">CMSG_KEY_AGREE_RECIPIENT_INFO</a> structure that identifies a key agreement recipient. Used for Diffie-Hellman recipients.

### -field DUMMYUNIONNAME.pMailList

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_mail_list_recipient_info">CMSG_MAIL_LIST_RECIPIENT_INFO</a> structure that identifies a recipient using a previously distributed key encryption key for the encryption/decryption of the envelopes message's <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a>.