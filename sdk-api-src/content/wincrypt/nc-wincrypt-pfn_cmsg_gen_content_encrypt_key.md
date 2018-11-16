---
UID: NC:wincrypt.PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
title: PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
author: windows-sdk-content
description: Generates the symmetric key used to encrypt content for an enveloped message.
old-location: security\pfn_cmsg_gen_content_encrypt_key.htm
tech.root: SecCrypto
ms.assetid: f06d0efb-44e1-40ed-9480-35dbdfce934c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY, PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback, PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback function [Security], security.pfn_cmsg_gen_content_encrypt_key, wincrypt/PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback function


## -description


The <b>PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY</b> callback function generates the symmetric key used to encrypt content for an enveloped message. This function is called by the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function when it initializes the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure.


## -parameters




### -param pContentEncryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the key.


### -param dwFlags [in]

This value is not used. Set it to zero.


### -param *pvReserved

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.






## -remarks



You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs). Which function is called depends on the value of the  <b>fCNG</b> member of the <a href="https://msdn.microsoft.com/c53014a0-049c-42ef-b612-8a1e03fb0dfd">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the  <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>CMSG_OID_GEN_CONTENT_ENCRYPT_KEY_FUNC or CMSG_OID_CAPI1_GEN_CONTENT_ENCRYPT_KEY_FUNC </td>
<td>"CryptMsgDllGenContentEncryptKey"</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>CMSG_OID_CNG_GEN_CONTENT_ENCRYPT_KEY_FUNC</td>
<td>"CryptMsgDllCNGGenContentEncryptKey"</td>
</tr>
</table>
 



