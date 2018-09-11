---
UID: NS:wincrypt._CRYPT_TIMESTAMP_CONTEXT
title: "_CRYPT_TIMESTAMP_CONTEXT"
author: windows-sdk-content
description: Contains both the encoded and decoded representations of a time stamp token.
old-location: security\crypt_timestamp_context.htm
tech.root: seccrypto
ms.assetid: 2831b2a9-0f84-4e41-a666-5903fc882965
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCRYPT_TIMESTAMP_CONTEXT, CRYPT_TIMESTAMP_CONTEXT, CRYPT_TIMESTAMP_CONTEXT structure [Security], PCRYPT_TIMESTAMP_CONTEXT, PCRYPT_TIMESTAMP_CONTEXT structure pointer [Security], _CRYPT_TIMESTAMP_CONTEXT, security.crypt_timestamp_context, wincrypt/CRYPT_TIMESTAMP_CONTEXT, wincrypt/PCRYPT_TIMESTAMP_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - CRYPT_TIMESTAMP_CONTEXT
product: Windows
targetos: Windows
req.typenames: CRYPT_TIMESTAMP_CONTEXT, *PCRYPT_TIMESTAMP_CONTEXT
req.redist: 
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

