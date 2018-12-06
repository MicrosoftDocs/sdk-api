---
UID: NF:bcrypt.BCryptHash
title: BCryptHash function
author: windows-sdk-content
description: Performs a single hash computation. This is a convenience function that wraps calls to BCryptCreateHash, BCryptHashData, BCryptFinishHash, and BCryptDestroyHash.
old-location: security\bcrypthash.htm
tech.root: seccng
ms.assetid: F0FF9B6D-1345-480A-BE13-BE90547407BF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BCryptHash, BCryptHash function [Security], bcrypt/BCryptHash, security.bcrypthash
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bcrypt.dll
api_name:
 - BCryptHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCryptHash function


## -description


Performs a single hash computation. This is a convenience function that wraps calls to <a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a>, <a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>, <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>, and <a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a>.


## -parameters




### -param hAlgorithm

The handle of an algorithm provider created by using the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function. The algorithm that was specified when the provider was created must support the hash interface.


### -param pbSecret

 A pointer to a buffer that contains the key to use for the hash or MAC. The <i>cbSecret</i> parameter contains the size of this buffer. This key only applies to hash algorithms opened by the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function by using the <b>BCRYPT_ALG_HANDLE_HMAC</b> flag.  Otherwise, set this parameter to <b>NULL</b>


### -param cbSecret

The size, in bytes, of the <i>pbSecret</i> buffer. If no key is used, set this parameter to zero.


### -param pbInput

A pointer to a buffer that contains the data to process. The <i>cbInput</i> parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.


### -param cbInput

The number of bytes in the <i>pbInput</i> buffer.


### -param pbOutput

A pointer to a buffer that receives the hash or MAC value. The <i>cbOutput</i> parameter contains the size of this buffer.


### -param cbOutput

The size, in bytes, of the <i>pbOutput</i> buffer. This size must exactly match the size of the hash or MAC value.

The size can be obtained by calling the <a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a> function to get the <b>BCRYPT_HASH_LENGTH</b> property. This will provide the size of the hash or MAC value for the specified algorithm.


## -returns



A status code indicating success or failure.



