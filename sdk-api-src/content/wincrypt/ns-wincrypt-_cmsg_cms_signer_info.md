---
UID: NS:wincrypt._CMSG_CMS_SIGNER_INFO
title: "_CMSG_CMS_SIGNER_INFO"
author: windows-sdk-content
description: Contains the content of the defined SignerInfo in signed or signed and enveloped messages.
old-location: security\cmsg_cms_signer_info.htm
old-project: SecCrypto
ms.assetid: 177323ef-4e26-4681-a474-1a99fb6900af
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PCMSG_CMS_SIGNER_INFO, CMSG_CMS_SIGNER_INFO, CMSG_CMS_SIGNER_INFO structure [Security], PCMSG_CMS_SIGNER_INFO, PCMSG_CMS_SIGNER_INFO structure pointer [Security], _CMSG_CMS_SIGNER_INFO, _crypto2_cmsg_cms_signer_info, security.cmsg_cms_signer_info, wincrypt/CMSG_CMS_SIGNER_INFO, wincrypt/PCMSG_CMS_SIGNER_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
req.typenames: CMSG_CMS_SIGNER_INFO, *PCMSG_CMS_SIGNER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_CMS_SIGNER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_CMS_SIGNER_INFO structure


## -description


The <b>CMSG_CMS_SIGNER_INFO</b> structure contains the content of the defined SignerInfo in signed or signed and enveloped messages. In decoding a received message, 
<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a> is called for each signer to get a <b>CMSG_CMS_SIGNER_INFO</b> structure.


## -struct-fields




### -field dwVersion

The version of this structure.


### -field SignerId

A <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure that identifies the signer's certificate.


### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used in generating the hash of a message.


### -field HashEncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to encrypt the hash.


### -field EncryptedHash

A
						<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encrypted hash of the message, the signature.


### -field AuthAttrs

A <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure that contains authenticated attributes of the signer.


### -field UnauthAttrs

A <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure that contains unauthenticated attributes of the signer.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

