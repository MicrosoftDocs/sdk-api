---
UID: NS:wincrypt._CRYPT_DECRYPT_MESSAGE_PARA
title: "_CRYPT_DECRYPT_MESSAGE_PARA"
author: windows-sdk-content
description: The CRYPT_DECRYPT_MESSAGE_PARA structure contains information for decrypting messages.
old-location: security\crypt_decrypt_message_para.htm
old-project: seccrypto
ms.assetid: 67e136cd-12e3-4a31-9d8b-b53e1129e940
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PCRYPT_DECRYPT_MESSAGE_PARA, CRYPT_DECRYPT_MESSAGE_PARA, CRYPT_DECRYPT_MESSAGE_PARA structure [Security], PCRYPT_DECRYPT_MESSAGE_PARA, PCRYPT_DECRYPT_MESSAGE_PARA structure pointer [Security], _CRYPT_DECRYPT_MESSAGE_PARA, _crypto2_crypt_decrypt_message_para, security.crypt_decrypt_message_para, wincrypt/CRYPT_DECRYPT_MESSAGE_PARA, wincrypt/PCRYPT_DECRYPT_MESSAGE_PARA"
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
tech.root: 
req.typenames: CRYPT_DECRYPT_MESSAGE_PARA, *PCRYPT_DECRYPT_MESSAGE_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_DECRYPT_MESSAGE_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_DECRYPT_MESSAGE_PARA structure


## -description



			The <b>CRYPT_DECRYPT_MESSAGE_PARA</b> structure contains information for decrypting messages.


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

### -field cCertStore

Number of elements in the <b>rghCertStore</b> array.


### -field rghCertStore

Array of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> handles. 




These certificate store handles are used to obtain the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> to use for decrypting a message. For more information, see the decryption functions 
<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>, and 
<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>. An encrypted message can have one or more recipients. The recipients are identified by a unique certificate identifier, often the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate issuer and serial number. The certificate stores are searched to find a certificate context corresponding to the unique identifier.

Recipients can also be identified by their KeyId. Both Key Agreement (Diffie-Hellman) and Key Transport (RSA) recipients are supported.

Only certificate contexts in the store with one of the following properties, CERT_KEY_PROV_INFO_PROP_ID, or CERT_KEY_CONTEXT_PROP_ID can be used. These properties specify the location of a needed private exchange key.


### -field dwFlags

The CRYPT_MESSAGE_SILENT_KEYSET_FLAG can be set to suppress any UI by the CSP. For more information about the CRYPT_SILENT flag, see 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>.


## -see-also




<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>
 

 

