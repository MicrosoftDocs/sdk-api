---
UID: NC:wincrypt.PFN_CMSG_CNG_IMPORT_KEY_AGREE
title: PFN_CMSG_CNG_IMPORT_KEY_AGREE
author: windows-sdk-content
description: Decrypts a content encryption key (CEK) that is intended for a key agreement recipient.
old-location: security\pfn_cmsg_cng_import_key_agree.htm
tech.root: seccrypto
ms.assetid: 407fddaa-8b7d-4ef4-bfc8-0b7a273905e7
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PFN_CMSG_CNG_IMPORT_KEY_AGREE, PFN_CMSG_CNG_IMPORT_KEY_AGREE callback, PFN_CMSG_CNG_IMPORT_KEY_AGREE callback function [Security], security.pfn_cmsg_cng_import_key_agree, wincrypt/PFN_CMSG_CNG_IMPORT_KEY_AGREE
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
 - PFN_CMSG_CNG_IMPORT_KEY_AGREE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CMSG_CNG_IMPORT_KEY_AGREE callback function


## -description


The <b>PFN_CMSG_CNG_IMPORT_KEY_AGREE</b> callback function decrypts a content encryption key (CEK) that is intended for a key agreement recipient. <b>PFN_CMSG_CNG_IMPORT_KEY_AGREE</b> can be installed by using a Cryptography API: Next Generation (CNG) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).


## -parameters




### -param pCNGContentDecryptInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/56e94b20-9d0a-4694-973f-a5878ad54f48">CMSG_CNG_CONTENT_DECRYPT_INFO</a> structure to be updated with the decrypted CEK bytes. This parameter contains the key used to decrypt the CEK.
The following <i>pKeyTransDecryptPara</i> parameter contains the 	CEK bytes to be decrypted.


### -param pKeyAgreeDecryptPara [in]

A pointer to a <a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_AGREE_DECRYPT_PARA</a> structure that contains the key agreement information passed to the <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> function in the <b>CMSG_CTRL_KEY_AGREE_DECRYPT</b> case.

The
<b>EncryptedKey</b> member of the <b>pKeyAgree</b> member contains the CEK bytes to be decrypted. Because a 
<a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_AGREE_DECRYPT_PARA</a> structure might contain an <b>HCRYPTPROV</b> choice, its <b>hNCryptKey</b> member must not be used to decrypt <b>EncryptedKey</b>. Instead, you must use the <b>hNCryptKey</b> member specified in the <i>pCNGContentDecryptInfo</i> parameter.


This function must not update members of the  <a href="https://msdn.microsoft.com/5f3387c9-4ff0-42a0-8fc7-67d3bb8b6bef">CMSG_CTRL_KEY_AGREE_DECRYPT_PARA</a> structure.


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

<b>CMSG_CTRL_KEY_AGREE_DECRYPT</b>
You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_CNG_IMPORT_KEY_AGREE_FUNC</td>
<td>"CryptMsgDllCNGImportKeyAgree"</td>
</tr>
</table>
 


#### Examples

For an example that deploys an OID-installable callback function, see <a href="https://msdn.microsoft.com/41c1758d-1213-47a6-81d5-7755b41c3007">Extending CryptoAPI Functionality</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cb71ea3a-0edd-4d46-8088-a395fab89d2b">Decoding Enveloped Data</a>
 

 

