---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CRYPT_TIMESTAMP_CONTEXT structure


## -description


The <b>CRYPT_TIMESTAMP_CONTEXT</b> structure contains both the encoded and decoded representations of a time stamp token. 


## -struct-fields




### -field cbEncoded

The size, in bytes, of the buffer pointed to by the <b>pbEncoded</b> member.


### -field pbEncoded

A pointer to a buffer that contains an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoded content information sequence. This value should be stored for future time stamp validations on the signature. Applications can use the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function  with the <b>CERT_STORE_PROV_PKCS7</b> flag to find additional certificates or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) related to the TSA time stamp signature.


### -field pTimeStamp

A pointer to a <a href="https://msdn.microsoft.com/05ca0877-5e9d-4b21-9fca-a1eef2cb4626">CRYPT_TIMESTAMP_INFO</a> structure that contains a signed data content type in Cryptographic Message Syntax (CMS) format.

