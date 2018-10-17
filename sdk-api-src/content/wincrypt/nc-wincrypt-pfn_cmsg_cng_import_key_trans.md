---
UID: NC:wincrypt.PFN_CMSG_CNG_IMPORT_KEY_TRANS
title: PFN_CMSG_CNG_IMPORT_KEY_TRANS
author: windows-sdk-content
description: Imports and decrypts a content encryption key (CEK) that is intended for a key transport recipient.
old-location: security\pfn_cmsg_cng_import_key_trans.htm
tech.root: seccrypto
ms.assetid: e03d86e3-4ace-4425-8aae-e3b4721cb9cc
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: PFN_CMSG_CNG_IMPORT_KEY_TRANS, PFN_CMSG_CNG_IMPORT_KEY_TRANS callback, PFN_CMSG_CNG_IMPORT_KEY_TRANS callback function [Security], security.pfn_cmsg_cng_import_key_trans, wincrypt/PFN_CMSG_CNG_IMPORT_KEY_TRANS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PFN_CMSG_CNG_IMPORT_KEY_TRANS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_CNG_IMPORT_KEY_TRANS callback function


## -description


The <b>PFN_CMSG_CNG_IMPORT_KEY_TRANS</b> callback function imports and decrypts a content encryption key (CEK) that is intended for a key transport recipient. <b>PFN_CMSG_CNG_IMPORT_KEY_TRANS</b> can be installed by using a Cryptography API: Next Generation (CNG) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).


## -parameters




### -param pCNGContentDecryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/56e94b20-9d0a-4694-973f-a5878ad54f48">CMSG_CNG_CONTENT_DECRYPT_INFO</a> structure to be updated with the decrypted CEK bytes. This parameter contains the key used to decrypt the CEK.
The following <i>pKeyTransDecryptPara</i> parameter contains the 	CEK bytes to be decrypted.


### -param pKeyTransDecryptPara [in]

A pointer to a <a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure that contains the key transport information passed to the <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> function in the <b>CMSG_CTRL_DECRYPT</b> or <b>CMSG_CTRL_KEY_TRANS_DECRYPT</b> cases. For the <b>CMSG_CTRL_DECRYPT</b> case, <b>CryptMsgControl</b> converts the <a href="https://msdn.microsoft.com/eb9b1daa-b04f-419a-88e3-7c772f9e62eb">CMSG_CTRL_DECRYPT_PARA</a> structure to a <b>CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</b> structure. 

The
<b>EncryptedKey</b> member of the <b>pKeyTrans</b> member contains the CEK bytes to be decrypted. Because a 
<a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure might contain an <b>HCRYPTPROV</b> choice, its <b>hNCryptKey</b> member must not be used to decrypt <b>EncryptedKey</b>. Instead, you must use the <b>hNCryptKey</b> specified in the <i>pCNGContentDecryptInfo</i> parameter.


This function must not update members of the  <a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_TRANS_DECRYPT_PARA</a> structure.


### -param dwFlags [in]

This parameter is reserved. Set it to zero.


### -param *pvReserved

This parameter is reserved. Set it to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



If this callback function does not support the key encryption algorithm, it must return <b>FALSE</b> and call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with ERROR_NOT_SUPPORTED.





## -remarks



The <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> function calls this function for the following operations specified by the <i>dwCtrlType</i> parameter:

<b>CMSG_CTRL_DECRYPT</b>
<b>CMSG_CTRL_KEY_TRANS_DECRYPT</b>
You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_CNG_IMPORT_KEY_TRANS_FUNC</td>
<td>"CryptMsgDllCNGImportKeyTrans"</td>
</tr>
</table>
 


#### Examples

For an example that deploys an OID-installable callback function, see <a href="https://msdn.microsoft.com/41c1758d-1213-47a6-81d5-7755b41c3007">Extending CryptoAPI Functionality</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cb71ea3a-0edd-4d46-8088-a395fab89d2b">Decoding Enveloped Data</a>
 

 

