---
UID: NE:bcrypt.HASHALGORITHM_ENUM
title: HASHALGORITHM_ENUM
author: windows-sdk-content
description: Specifies signing and hashing algorithms.
old-location: security\hashalgorithm_enum.htm
old-project: seccng
ms.assetid: 482DA4B6-EC1C-4E88-95C0-62ED1356DC3B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DSA_HASH_ALGORITHM_SHA1, DSA_HASH_ALGORITHM_SHA256, DSA_HASH_ALGORITHM_SHA512, HASHALGORITHM_ENUM, HASHALGORITHM_ENUM enumeration [Security], bcrypt/DSA_HASH_ALGORITHM_SHA1, bcrypt/DSA_HASH_ALGORITHM_SHA256, bcrypt/DSA_HASH_ALGORITHM_SHA512, bcrypt/HASHALGORITHM_ENUM, security.hashalgorithm_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: bcrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: HASHALGORITHM_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - HASHALGORITHM_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

