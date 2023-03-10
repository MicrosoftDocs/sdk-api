---
UID: NS:wincrypt._CMSG_RECIPIENT_ENCODE_INFO
title: CMSG_RECIPIENT_ENCODE_INFO (wincrypt.h)
description: Contains information a message recipient's content encryption key management type.
helpviewer_keywords: ["*PCMSG_RECIPIENT_ENCODE_INFO","CMSG_KEY_AGREE_RECIPIENT","CMSG_KEY_TRANS_RECIPIENT","CMSG_MAIL_LIST_RECIPIENT","CMSG_RECIPIENT_ENCODE_INFO","CMSG_RECIPIENT_ENCODE_INFO structure [Security]","PCMSG_RECIPIENT_ENCODE_INFO","PCMSG_RECIPIENT_ENCODE_INFO structure [Security]","_crypto2_cmsg_recipient_encode_info","security.cmsg_recipient_encode_info","wincrypt/CMSG_RECIPIENT_ENCODE_INFO","wincrypt/PCMSG_RECIPIENT_ENCODE_INFO"]
old-location: security\cmsg_recipient_encode_info.htm
tech.root: security
ms.assetid: eb85f3e4-a5f8-45e7-9bbf-9c649db1e141
ms.date: 12/05/2018
ms.keywords: '*PCMSG_RECIPIENT_ENCODE_INFO, CMSG_KEY_AGREE_RECIPIENT, CMSG_KEY_TRANS_RECIPIENT, CMSG_MAIL_LIST_RECIPIENT, CMSG_RECIPIENT_ENCODE_INFO, CMSG_RECIPIENT_ENCODE_INFO structure [Security], PCMSG_RECIPIENT_ENCODE_INFO, PCMSG_RECIPIENT_ENCODE_INFO structure [Security], _crypto2_cmsg_recipient_encode_info, security.cmsg_recipient_encode_info, wincrypt/CMSG_RECIPIENT_ENCODE_INFO, wincrypt/PCMSG_RECIPIENT_ENCODE_INFO'
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
req.typenames: CMSG_RECIPIENT_ENCODE_INFO, *PCMSG_RECIPIENT_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_RECIPIENT_ENCODE_INFO
 - wincrypt/_CMSG_RECIPIENT_ENCODE_INFO
 - PCMSG_RECIPIENT_ENCODE_INFO
 - wincrypt/PCMSG_RECIPIENT_ENCODE_INFO
 - CMSG_RECIPIENT_ENCODE_INFO
 - wincrypt/CMSG_RECIPIENT_ENCODE_INFO
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
 - CMSG_RECIPIENT_ENCODE_INFO
---

# CMSG_RECIPIENT_ENCODE_INFO structure


## -description

The <b>CMSG_RECIPIENT_ENCODE_INFO</b> structure contains information a message recipient's content encryption key management type.
<div class="alert"><b>Note</b>  Only key transport recipients are supported in PKCS #7 version 1.5.</div><div> </div>

## -struct-fields

### -field dwRecipientChoice

Indicates the union member to be used. The following values are defined.

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
Use with key transport key management

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_RECIPIENT"></a><a id="cmsg_key_agree_recipient"></a><dl>
<dt><b>CMSG_KEY_AGREE_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
Used with key agreement key management

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_MAIL_LIST_RECIPIENT"></a><a id="cmsg_mail_list_recipient"></a><dl>
<dt><b>CMSG_MAIL_LIST_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
Use with previously distributed key encryption key management

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pKeyTrans

A pointer to a 
<a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_key_trans_recipient_encode_info">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_KEY_TRANS_RECIPIENT

### -field DUMMYUNIONNAME.pKeyAgree

A pointer to a 
<a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_key_agree_recipient_encode_info">CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_KEY_AGREE_RECIPIENT

### -field DUMMYUNIONNAME.pMailList

A pointer to a 
<a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_mail_list_recipient_encode_info">CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_MAIL_LIST_RECIPIENT

