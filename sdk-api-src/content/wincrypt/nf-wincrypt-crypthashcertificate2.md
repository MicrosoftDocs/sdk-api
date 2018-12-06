---
UID: NF:wincrypt.CryptHashCertificate2
title: CryptHashCertificate2 function
author: windows-sdk-content
description: Hashes a block of data by using a CNG hash provider.
old-location: security\crypthashcertificate2.htm
tech.root: seccrypto
ms.assetid: 9f315374-0002-499a-81ea-efcb3c19e68f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptHashCertificate2, CryptHashCertificate2 function [Security], security.crypthashcertificate2, wincrypt/CryptHashCertificate2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptHashCertificate2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptHashCertificate2 function


## -description


The <b>CryptHashCertificate2</b> function hashes a block of data by using a CNG hash provider.


## -parameters




### -param pwszCNGHashAlgid [in]

The address of a null-terminated Unicode string that contains the CNG hash algorithm identifier of the hash algorithm to use to hash the certificate. This can be one of the <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> that represents a hash algorithm or any other registered hash algorithm identifier.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.


### -param pvReserved

Reserved for future use and must be <b>NULL</b>.


### -param pbEncoded [in]

The address of an array of bytes to be hashed. The <i>cbEncoded</i> parameter contains the size of this array.


### -param cbEncoded [in]

The number of elements in the <i>pbEncoded</i> array.


### -param pbComputedHash [out]

The address of a buffer that receives the computed hash. The variable pointed to by the <i>pcbComputedHash</i> parameter contains the size of this buffer.


### -param pcbComputedHash [in, out]

The address of a <b>DWORD</b> variable that, on entry, contains the size, in bytes, of the  <i>pbComputedHash</i> buffer. After this function returns, this variable contains the number of bytes copied to the <i>pbComputedHash</i> buffer.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some of the possible error codes are identified in the following topics.<dl>
<dd>
<a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>
</dd>
</dl>





## -see-also




<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

