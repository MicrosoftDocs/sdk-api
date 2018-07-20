---
UID: NS:wincrypt._CMSG_SIGNER_INFO
title: "_CMSG_SIGNER_INFO"
author: windows-sdk-content
description: The CMSG_SIGNER_INFO structure contains the content of the PKCS #7 defined SignerInfo in signed messages. In decoding a received message, CryptMsgGetParam is called for each signer to get a CMSG_SIGNER_INFO structure.
old-location: security\cmsg_signer_info.htm
old-project: seccrypto
ms.assetid: eae631d2-5e5f-4964-b079-9692831b34fc
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PCMSG_SIGNER_INFO, CMSG_SIGNER_INFO, CMSG_SIGNER_INFO structure [Security], PCMSG_SIGNER_INFO, PCMSG_SIGNER_INFO structure pointer [Security], _CMSG_SIGNER_INFO, _crypto2_cmsg_signer_info, security.cmsg_signer_info, wincrypt/CMSG_SIGNER_INFO, wincrypt/PCMSG_SIGNER_INFO"
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
req.typenames: CMSG_SIGNER_INFO, *PCMSG_SIGNER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_SIGNER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_SIGNER_INFO structure


## -description


The <b>CMSG_SIGNER_INFO</b> structure contains the content of the PKCS #7 defined SignerInfo in signed messages. In decoding a received message, 
<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a> is called for each signer to get a <b>CMSG_SIGNER_INFO</b> structure.


## -struct-fields




### -field dwVersion

The version of this structure.


### -field Issuer


						A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structure that contains the issuer of a certificate with the public key needed to verify a signature.


### -field SerialNumber


						A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate that contains the public key needed to verify a signature. For more information, see 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>.


### -field HashAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure specifying the algorithm used in generating the hash of a message.


### -field HashEncryptionAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure specifying the algorithm used to encrypt the hash.


### -field EncryptedHash

A
						<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> that contains the encrypted hash of the message, the signature.


### -field AuthAttrs


<a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure containing authenticated attributes of the signer.


### -field UnauthAttrs


<a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure containing unauthenticated attributes of the signer.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

