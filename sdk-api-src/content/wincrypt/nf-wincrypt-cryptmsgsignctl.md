---
UID: NF:wincrypt.CryptMsgSignCTL
title: CryptMsgSignCTL function
author: windows-driver-content
description: The CryptMsgSignCTL function creates a signed message containing an encoded CTL.
old-location: security\cryptmsgsignctl.htm
old-project: SecCrypto
ms.assetid: 85ae8ce3-d0a7-4fcb-beaa-ede09d30930e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CryptMsgSignCTL, CryptMsgSignCTL function [Security], _crypto2_cryptmsgsignctl, security.cryptmsgsignctl, wincrypt/CryptMsgSignCTL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptMsgSignCTL
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMsgSignCTL function


## -description



			The <b>CryptMsgSignCTL</b> function creates a signed message containing an encoded CTL.


## -parameters




### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCtlContent [in]

The encoded 
<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a> that can be a member of a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure or can be created using the 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> function.


### -param cbCtlContent [in]

The size, in bytes, of the content pointed to by <i>pbCtlContent</i>.


### -param pSignInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure containing an array of a 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures.

The message can be encoded without signers if the <b>cbSize</b> member of the structure is set to the size of the structure and all of the other members are set to zero.


### -param dwFlags [in]

If CMS_PKCS7 is defined, can be set to CMSG_CMS_ENCAPSULATED_CTL_FLAG to encode a CMS compatible V3 SignedData message.


### -param pbEncoded [out]

A pointer to a buffer to receives the encoded message.

This parameter can be <b>NULL</b> to get the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbEncoded</i> buffer. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. This function can return errors propagated from calls to 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> and 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>.




## -see-also




<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/5c0e9e2e-a50d-45d0-b51d-065784d1d912">CryptMsgEncodeAndSignCTL</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="cryptography_functions.htm">Verification Functions Using CTLs</a>
 

 

