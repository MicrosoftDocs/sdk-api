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

# _CMSG_CMS_RECIPIENT_INFO structure


## -description


The <b>CMSG_CMS_RECIPIENT_INFO</b> structure is used with the 
<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a> function to get information on a key transport, key agreement, or mail list envelope message recipient. This structure is returned in <i>pvData</i> when <a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a> is called with <i>dwParamType</i> set to CMSG_CMS_RECIPIENT_INFO_PARAM.


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
<a href="https://msdn.microsoft.com/956b0646-50a5-46d1-aa9a-91194c35d2b2">CMSG_KEY_TRANS_RECIPIENT_INFO</a> structure that identifies a key transport recipient. Used for RSA recipients.


### -field DUMMYUNIONNAME.pKeyAgree

A pointer to a 
<a href="https://msdn.microsoft.com/d29d04d6-065e-4bb7-843b-f563643eeb4c">CMSG_KEY_AGREE_RECIPIENT_INFO</a> structure that identifies a key agreement recipient. Used for Diffie-Hellman recipients.


### -field DUMMYUNIONNAME.pMailList

A pointer to a 
<a href="https://msdn.microsoft.com/e0946278-75e9-4990-af81-d9e61da9724b">CMSG_MAIL_LIST_RECIPIENT_INFO</a> structure that identifies a recipient using a previously distributed key encryption key for the encryption/decryption of the envelopes message's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a>.

