---
UID: NC:wincrypt.PFN_CMSG_EXPORT_KEY_TRANS
title: PFN_CMSG_EXPORT_KEY_TRANS
author: windows-sdk-content
description: Encrypts and exports the content encryption key for a key transport recipient of an enveloped message.
old-location: security\pfn_cmsg_export_key_trans.htm
tech.root: seccrypto
ms.assetid: bbb976df-5c8d-4d5e-ba92-7c534bba59de
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PFN_CMSG_EXPORT_KEY_TRANS, PFN_CMSG_EXPORT_KEY_TRANS callback, PFN_CMSG_EXPORT_KEY_TRANS callback function [Security], security.pfn_cmsg_export_key_trans, wincrypt/PFN_CMSG_EXPORT_KEY_TRANS
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
 - PFN_CMSG_EXPORT_KEY_TRANS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_EXPORT_KEY_TRANS callback function


## -description


The <b>PFN_CMSG_EXPORT_KEY_TRANS</b> callback function encrypts and exports the content encryption key for a key transport recipient of an enveloped message. <b>PFN_CMSG_EXPORT_KEY_TRANS</b> can be installed by using a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a> <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This function is called by the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.


## -parameters




### -param pContentEncryptInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.


### -param pKeyTransEncodeInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/20b20759-3d76-4814-9e71-7376dd326f7b">CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</a> structure that specifies the recipient public key used to encrypt the content encryption key.


### -param pKeyTransEncryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/f3122acb-92c8-4803-8c74-8b3a2cf2e16e">CMSG_KEY_TRANS_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.


### -param dwFlags [in]

This value is not used. Set it to zero.


### -param *pvReserved

This value is reserved. Set it to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.






## -remarks



The <b>PFN_CMSG_EXPORT_KEY_TRANS</b> function must update the <b>EncryptedKey</b> member of the <a href="https://msdn.microsoft.com/f3122acb-92c8-4803-8c74-8b3a2cf2e16e">CMSG_KEY_TRANS_ENCRYPT_INFO</a> structure pointed to by the <i>pKeyTransEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory allocation for the encrypted key.

You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different OIDs. Which function is called depends on the value of the <b>fCNG</b> member of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>FALSE</td>
<td>CMSG_OID_EXPORT_KEY_TRANS_FUNC or CMSG_OID_CAPI1_EXPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllExportKeyTrans"</td>
</tr>
<tr>
<td>TRUE</td>
<td>CMSG_OID_CNG_EXPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllCNGExportKeyTrans"</td>
</tr>
</table>
 



