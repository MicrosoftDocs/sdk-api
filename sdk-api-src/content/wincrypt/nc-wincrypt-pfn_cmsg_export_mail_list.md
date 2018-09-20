---
UID: NC:wincrypt.PFN_CMSG_EXPORT_MAIL_LIST
title: PFN_CMSG_EXPORT_MAIL_LIST
author: windows-sdk-content
description: Encrypts and exports the content encryption key for a mailing list recipient of an enveloped message.
old-location: security\pfn_cmsg_export_mail_list.htm
tech.root: seccrypto
ms.assetid: 68a75714-cf47-40f9-95ab-e1ffc8936390
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: PFN_CMSG_EXPORT_MAIL_LIST, PFN_CMSG_EXPORT_MAIL_LIST callback, PFN_CMSG_EXPORT_MAIL_LIST callback function [Security], security.pfn_cmsg_export_mail_list, wincrypt/PFN_CMSG_EXPORT_MAIL_LIST
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
 - PFN_CMSG_EXPORT_MAIL_LIST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_EXPORT_MAIL_LIST callback function


## -description


The <b>PFN_CMSG_EXPORT_MAIL_LIST</b> callback function encrypts and exports the content encryption key for a mailing list recipient of an enveloped message. <b>PFN_CMSG_EXPORT_MAIL_LIST</b> can be installed by using a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a> <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This function is called by the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.


## -parameters




### -param pContentEncryptInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.


### -param pMailListEncodeInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/4303a7e7-cb93-4ed1-85e6-42359c2c687c">CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</a> structure that specifies the key used to encrypt the content encryption key.


### -param pMailListEncryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/25c4338a-1ea3-4fff-a6bf-f3884a8154d3">CMSG_MAIL_LIST_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.


### -param dwFlags [in]

This value is not used. Set it to zero.


### -param *pvReserved

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.






## -remarks



The <b>PFN_CMSG_EXPORT_MAIL_LIST</b> function must update the  <b>EncryptedKey</b> member of the <a href="https://msdn.microsoft.com/25c4338a-1ea3-4fff-a6bf-f3884a8154d3">CMSG_MAIL_LIST_ENCRYPT_INFO</a> structure pointed to by the <i>pMailListEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory for any values that it updates.

You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_EXPORT_MAIL_LIST_FUNC or CMSG_OID_CAPI1_EXPORT_MAIL_LIST_FUNC</td>
<td>"CryptMsgDllExportMailList"</td>
</tr>
</table>
 



