---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CMSG_RECIPIENT_ENCODE_INFO structure


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
<a href="https://msdn.microsoft.com/20b20759-3d76-4814-9e71-7376dd326f7b">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_KEY_TRANS_RECIPIENT


### -field DUMMYUNIONNAME.pKeyAgree

A pointer to a 
<a href="https://msdn.microsoft.com/f8691df7-3cc1-48cb-8787-84c7046b280f">CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_KEY_AGREE_RECIPIENT


### -field DUMMYUNIONNAME.pMailList

A pointer to a 
<a href="https://msdn.microsoft.com/4303a7e7-cb93-4ed1-85e6-42359c2c687c">CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</a> structure. Used with CMSG_MAIL_LIST_RECIPIENT

