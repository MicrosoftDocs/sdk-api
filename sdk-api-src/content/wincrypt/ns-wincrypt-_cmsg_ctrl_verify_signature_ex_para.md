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

# _CMSG_CTRL_VERIFY_SIGNATURE_EX_PARA structure


## -description


The <b>CMSG_CTRL_VERIFY_SIGNATURE_EX_PARA</b> structure contains information used to verify a message signature. It contains the signer index and signer public key. The signer public key can be the signer's <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, or chain context.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic provider</a> used to verify the signature. If <b>NULL</b>, the cryptographic provider specified in <a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a> is used. If the <i>hCryptProv</i> in <b>CryptMsgOpenToDecode</b> is also <b>NULL</b>, the default provider according to the signer's public key <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) is used.This member's data type is <b>HCRYPTPROV</b>.




### -field dwSignerIndex

The index of the signer in the message.


### -field dwSignerType

The structure that contains the signer information. The following table shows the predefined values and the structures indicated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_VERIFY_SIGNER_PUBKEY"></a><a id="cmsg_verify_signer_pubkey"></a><dl>
<dt><b>CMSG_VERIFY_SIGNER_PUBKEY</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_VERIFY_SIGNER_CERT"></a><a id="cmsg_verify_signer_cert"></a><dl>
<dt><b>CMSG_VERIFY_SIGNER_CERT</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_VERIFY_SIGNER_CHAIN"></a><a id="cmsg_verify_signer_chain"></a><dl>
<dt><b>CMSG_VERIFY_SIGNER_CHAIN</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_VERIFY_SIGNER_NULL"></a><a id="cmsg_verify_signer_null"></a><dl>
<dt><b>CMSG_VERIFY_SIGNER_NULL</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
</table>
 


### -field pvSigner

A pointer to a <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure, a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, a chain context, or <b>NULL</b> depending on the value of <b>dwSignerType</b>.


## -remarks



If <b>dwSignerType</b> is CMSG_VERIFY_SIGNER_NULL, the signature is expected to contain only the unencrypted hash octets.



