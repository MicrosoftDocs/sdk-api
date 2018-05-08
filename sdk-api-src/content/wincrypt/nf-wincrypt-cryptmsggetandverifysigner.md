---
UID: NF:wincrypt.CryptMsgGetAndVerifySigner
title: CryptMsgGetAndVerifySigner function
author: windows-driver-content
description: The CryptMsgGetAndVerifySigner function verifies a cryptographic message's signature.
old-location: security\cryptmsggetandverifysigner.htm
old-project: SecCrypto
ms.assetid: 380c9cf3-27a2-4354-b1c8-97cec33f4e44
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: CMSG_SIGNER_ONLY_FLAG, CMSG_TRUSTED_SIGNER_FLAG, CMSG_USE_SIGNER_INDEX_FLAG, CryptMsgGetAndVerifySigner, CryptMsgGetAndVerifySigner function [Security], _crypto2_cryptmsggetandverifysigner, security.cryptmsggetandverifysigner, wincrypt/CryptMsgGetAndVerifySigner
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptMsgGetAndVerifySigner
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMsgGetAndVerifySigner function


## -description


The <b>CryptMsgGetAndVerifySigner</b> function verifies a cryptographic message's signature.


## -parameters




### -param hCryptMsg [in]

Handle of a cryptographic message.


### -param cSignerStore [in]

Number of stores in the <i>rghSignerStore</i> array.


### -param rghSignerStore [in, optional]

Array of certificate store handles that can be searched for a signer's certificate.


### -param dwFlags [in]

Indicates particular use of the function. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_TRUSTED_SIGNER_FLAG"></a><a id="cmsg_trusted_signer_flag"></a><dl>
<dt><b>CMSG_TRUSTED_SIGNER_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The stores in <i>rghSignerStore</i> are assumed trusted and they are the only stores searched to find the certificate corresponding to the signer's issuer and serial number. Otherwise, signer stores can be provided to supplement the message's store of certificates. If a signer certificate is found, its public key is used to verify the message signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNER_ONLY_FLAG"></a><a id="cmsg_signer_only_flag"></a><dl>
<dt><b>CMSG_SIGNER_ONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Return the signer without doing the signature verification.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_USE_SIGNER_INDEX_FLAG"></a><a id="cmsg_use_signer_index_flag"></a><dl>
<dt><b>CMSG_USE_SIGNER_INDEX_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Only the signer specified by *<i>pdwSignerIndex</i> is returned. Otherwise, iterate through all the signers until a signature is verified or there are no more signers.

</td>
</tr>
</table>
 


### -param ppSigner [out, optional]

If the signature is verified, <i>ppSigner</i> is updated to point to the signer's <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>. When you have finished using the certificate, free the context by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function. This parameter can be <b>NULL</b> if the application has no need for the signer's certificate.


### -param pdwSignerIndex [in, out, optional]

If the signature is verified, <i>pdwSigner</i> is updated to point to the index of the signer in the array of signers. This parameter can be <b>NULL</b> if the application has no need for the index of the signer.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>



<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a>



<a href="cryptography_functions.htm">Verification Functions Using CTLs</a>
 

 

