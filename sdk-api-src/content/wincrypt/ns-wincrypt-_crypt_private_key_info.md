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

# _CRYPT_PRIVATE_KEY_INFO structure


## -description


<p class="CCE_Message">[The <b>CRYPT_PRIVATE_KEY_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PRIVATE_KEY_INFO</b> structure contains a clear-text <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> in the PrivateKey field (DER
   encoded). <b>CRYPT_PRIVATE_KEY_INFO</b> contains the information in a PKCS #8 PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.


## -struct-fields




### -field Version

A <b>DWORD</b>  value that identifies the PKCS #8 version.


### -field Algorithm

A  <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>  structure that indicates the algorithm in which the private key (RSA or DSA) is to be used.


### -field PrivateKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains the key data.


### -field pAttributes

A <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a>  structure that identifies the PKCS #8 attributes.


## -see-also




<a href="https://msdn.microsoft.com/82fee86a-8704-4f22-8f11-f89509c5a0aa">CryptExportPKCS8Ex</a>



<a href="https://msdn.microsoft.com/d3b2b942-bde5-4399-9412-95fe227cd546">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>
 

 

