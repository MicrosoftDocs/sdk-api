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

# HASHALGORITHM_ENUM enumeration


## -description


The <b>HASHALGORITHM_ENUM</b> enumeration type specifies signing and hashing algorithms. It is used by the <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> and <a href="https://msdn.microsoft.com/25FF89D8-1E3E-433B-AC5C-1CADC09A49D0">BCRYPT_DSA_PARAMETER_HEADER_V2</a> structures.


## -enum-fields




### -field DSA_HASH_ALGORITHM_SHA1

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 1 (SHA1) to hash the message contents before signing.


### -field DSA_HASH_ALGORITHM_SHA256

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 256 (SHA256) to hash the message contents before signing.


### -field DSA_HASH_ALGORITHM_SHA512

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 512 (SHA512) to hash the message contents before signing.


## -see-also




<a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a>



<a href="https://msdn.microsoft.com/25FF89D8-1E3E-433B-AC5C-1CADC09A49D0">BCRYPT_DSA_PARAMETER_HEADER_V2</a>
 

 

