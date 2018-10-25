---
UID: NC:wincrypt.PFN_CMSG_IMPORT_KEY_TRANS
title: PFN_CMSG_IMPORT_KEY_TRANS
author: windows-sdk-content
description: Imports a content encryption key for a key transport recipient of an enveloped message.
old-location: security\pfn_cmsg_import_key_trans.htm
tech.root: seccrypto
ms.assetid: ad8051a9-a8ca-47fc-8b4c-d6c085ff1db8
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: PFN_CMSG_IMPORT_KEY_TRANS, PFN_CMSG_IMPORT_KEY_TRANS callback, PFN_CMSG_IMPORT_KEY_TRANS callback function [Security], security.pfn_cmsg_import_key_trans, wincrypt/PFN_CMSG_IMPORT_KEY_TRANS
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
 - PFN_CMSG_IMPORT_KEY_TRANS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_IMPORT_KEY_TRANS callback function


## -description


The <b>PFN_CMSG_IMPORT_KEY_TRANS</b> callback function imports a content encryption key for a key transport recipient of an enveloped message. <b>PFN_CMSG_IMPORT_KEY_TRANS</b> can be installed by using a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a> <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>. This function is called by the <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> function when its <i>dwCtrlType</i> parameter is set to <b>CMSG_CTRL_DECRYPT</b>.


## -parameters




### -param pContentEncryptionAlgorithm [in]

A pointer to a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to encrypt the message contents and any associated parameters.


### -param pKeyTransDecryptPara [in]

A pointer to a <a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure that contains information about the key transport recipient.


### -param dwFlags [in]

This value is not used. Set it to zero.


### -param *pvReserved

This parameter is reserved and must be <b>NULL</b>.


### -param *phContentEncryptKey [out]

The address of a handle to the content encryption key returned by this function.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



If this callback function does not support the key encryption algorithm, it must return <b>FALSE</b> and call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with <b>E_NOTIMPL</b>.




## -remarks



You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_IMPORT_KEY_TRANS_FUNC or CMSG_OID_CAPI1_IMPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllImportKeyTrans"</td>
</tr>
</table>
 



