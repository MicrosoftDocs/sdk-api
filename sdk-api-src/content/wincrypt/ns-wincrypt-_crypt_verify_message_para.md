---
UID: NS:wincrypt._CRYPT_VERIFY_MESSAGE_PARA
title: "_CRYPT_VERIFY_MESSAGE_PARA"
author: windows-sdk-content
description: The CRYPT_VERIFY_MESSAGE_PARA structure contains information needed to verify signed messages.
old-location: security\crypt_verify_message_para.htm
tech.root: seccrypto
ms.assetid: bbd56b5e-2bbe-420f-8842-1be50dca779f
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PCRYPT_VERIFY_MESSAGE_PARA, CRYPT_VERIFY_MESSAGE_PARA, CRYPT_VERIFY_MESSAGE_PARA structure [Security], PCRYPT_VERIFY_MESSAGE_PARA, PCRYPT_VERIFY_MESSAGE_PARA structure pointer [Security], _CRYPT_VERIFY_MESSAGE_PARA, _crypto2_crypt_verify_message_para, security.crypt_verify_message_para, wincrypt/CRYPT_VERIFY_MESSAGE_PARA, wincrypt/PCRYPT_VERIFY_MESSAGE_PARA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_VERIFY_MESSAGE_PARA
product: Windows
targetos: Windows
req.typenames: CRYPT_VERIFY_MESSAGE_PARA, *PCRYPT_VERIFY_MESSAGE_PARA
req.redist: 
---

# _CRYPT_VERIFY_MESSAGE_PARA structure


## -description


The <b>CRYPT_VERIFY_MESSAGE_PARA</b> structure contains information needed to verify signed messages.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwMsgAndCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> to be used to verify a signed message. The CSP identified by this handle is used for <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing</a> and for signature verification.Unless there is a strong reason for using a specific cryptographic provider, set to  zero to use the default RSA or DSS provider.

This member's data type is <b>HCRYPTPROV</b>.




### -field pfnGetSignerCertificate

A pointer to the callback function used to get the signer's certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>. If <b>NULL</b>, the default callback is used. The default callback tries to get the signer <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> from the message's <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.

An application defined–callback function that gets the signer's certificate can be used in place of the default. It is passed the certificate identifier of the signer (its issuer and serial number) and a handle to its cryptographic signed message's certificate store.

See <a href="https://msdn.microsoft.com/557ebb26-cce0-4c41-b49c-769b2831cf35">CryptGetSignerCertificateCallback</a> for the callback functions signature and arguments.


### -field pvGetArg

Argument to pass to the callback function. Typically, this gets and verifies the message signer's certificate.


### -field pStrongSignPara

Optional pointer to a <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure that contains parameters used for strong signing. If you set this member and the function successfully verifies the signature, the function will then check for a strong signature. If the signature is not strong, the operation will fail and set the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> value to <b>NTE_BAD_ALGID</b>.

<div class="alert"><b>Note</b>  You can use the <b>pStrongSignPara</b> member  only if <b>CRYPT_VERIFY_MESSAGE_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If <b>CRYPT_VERIFY_MESSAGE_PARA_HAS_EXTRA_FIELDS</b> is defined, you must zero all unused fields.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.


## -remarks



This structure is passed to the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/25ffd058-8f75-4ba5-b075-e3efc09f5d9d">CryptDecodeMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d437f6bf-eb56-4d29-bb91-eb8487e50219">CryptVerifyDetachedMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/d437f6bf-eb56-4d29-bb91-eb8487e50219">CryptVerifyDetachedMessageSignature</a>



<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>
 

 

