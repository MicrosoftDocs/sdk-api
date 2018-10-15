---
UID: NC:wincrypt.PFN_CMSG_EXPORT_KEY_AGREE
title: PFN_CMSG_EXPORT_KEY_AGREE
author: windows-sdk-content
description: Encrypts and exports the content encryption key for a key agreement recipient of an enveloped message.
old-location: security\pfn_cmsg_export_key_agree.htm
tech.root: seccrypto
ms.assetid: 5283f3be-7451-4896-82a5-bcfe63db9344
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PFN_CMSG_EXPORT_KEY_AGREE, PFN_CMSG_EXPORT_KEY_AGREE callback, PFN_CMSG_EXPORT_KEY_AGREE callback function [Security], security.pfn_cmsg_export_key_agree, wincrypt/PFN_CMSG_EXPORT_KEY_AGREE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CMSG_EXPORT_KEY_AGREE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_EXPORT_KEY_AGREE callback function


## -description


The <b>PFN_CMSG_EXPORT_KEY_AGREE</b> callback function encrypts and exports the content encryption key for a key agreement recipient of an enveloped message. <b>PFN_CMSG_EXPORT_KEY_AGREE</b> can be installed by using a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a> <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This function is called by the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.


## -parameters




### -param pContentEncryptInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.


### -param pKeyAgreeEncodeInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f8691df7-3cc1-48cb-8787-84c7046b280f">CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</a> structure that specifies the key used to encrypt the content encryption key.


### -param pKeyAgreeEncryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7604ac82-a1a2-451b-8615-98303ce1d83e">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.


### -param dwFlags [in]

This value is not used. Set it to zero.


### -param *pvReserved

This parameter is reserved and must be NULL.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.






## -remarks



For each recipient key, the <b>PFN_CMSG_EXPORT_KEY_AGREE</b> function must update the   <b>EncryptedKey</b> member of the <a href="https://msdn.microsoft.com/586d40cc-8ef6-475b-8b7b-cc1a0bdddfcb">CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</a> structure referred to by the <b>rgpKeyAgreeKeyEncryptInfo</b> member of the <a href="https://msdn.microsoft.com/7604ac82-a1a2-451b-8615-98303ce1d83e">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyAgreeEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory for any values that it updates.

If, upon entry,  the <b>dwEncryptFlags</b> member of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> member is set to <b>CMSG_CONTENT_ENCRYPT_PAD_ENCODED_LEN_FLAG</b>, the ephemeral <b>PublicKey</b> member of the <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure referred to by the <b>OriginatorPublicKeyInfo</b> member of the <a href="https://msdn.microsoft.com/7604ac82-a1a2-451b-8615-98303ce1d83e">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyAgreeEncryptInfo</i> parameter should be padded with zeros to always obtain the same maximum encoded length. <div class="alert"><b>Note</b>  The length of the generated ephemeral Y public key can vary depending on the number of leading zero bits.</div>
<div> </div>


You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different OIDs. Which function is called depends on the value of the  <b>fCNG</b> member of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>CMSG_OID_EXPORT_KEY_AGREE_FUNC or CMSG_OID_CAPI1_EXPORT_KEY_AGREE_FUNC</td>
<td>"CryptMsgDllExportKeyAgree"</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>CMSG_OID_CNG_EXPORT_KEY_AGREE_FUNC</td>
<td>"CryptMsgDllCNGExportKeyAgree"</td>
</tr>
</table>
 



