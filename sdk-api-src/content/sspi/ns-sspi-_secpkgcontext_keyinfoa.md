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

# _SecPkgContext_KeyInfoA structure


## -description



			The <b>SecPkgContext_KeyInfo</b> structure contains information about the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session keys</a> used in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.

Applications using the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) should not use the <b>SecPkgContext_KeyInfo</b> structure. Instead, use the <a href="https://msdn.microsoft.com/5380c03b-d2c5-4a0d-96a1-c39305b9c9ac">SecPkgContext_ConnectionInfo</a> structure.


## -struct-fields




### -field sSignatureAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for generating signatures, for example "MD5" or "SHA-2".


### -field sEncryptAlgorithmName

Pointer to a null-terminated string that contains the name, if available, of the algorithm used for encrypting messages. Reserved for future use.


### -field KeySize

Specifies the effective key length, in bits, for the session key. This is typically 40, 56, or 128 bits.


### -field SignatureAlgorithm

Specifies the algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>) used for generating signatures, if available.


### -field EncryptAlgorithm

Specifies the algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>) used for encrypting messages. Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>
 

 

