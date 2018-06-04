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

# _CRYPT_PKCS8_IMPORT_PARAMS structure


## -description


<p class="CCE_Message">[The <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure contains a PKCS #8 <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> and pointers to callback
functions. <b>CRYPT_PKCS8_IMPORT_PARAMS</b> is used by the <a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a> function. The first callback supplies the algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a> needed to  specify the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) into which the key will be imported. If the private key in PKCS #8 is encrypted, the <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure contains the encrypted private key, and the second callback is used to decrypt this private key.


## -struct-fields




### -field PrivateKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DIGEST_BLOB</a> structure that contains the PKCS #8 data.


### -field pResolvehCryptProvFunc

A <a href="https://msdn.microsoft.com/d3b2b942-bde5-4399-9412-95fe227cd546">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a> pointer  that points to data used by a user-defined function that retrieves a handle to a CSP.


### -field pVoidResolveFunc

An  <b>LPVOID</b>  value that identifies the function used to retrieve the CSP provider handle.


### -field pDecryptPrivateKeyFunc

A <a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a> pointer that points to  a callback function used to decrypt the private key.


### -field pVoidDecryptFunc

An <b>LPVOID</b> value that provides data used for encryption, such as key, initialization vector, and password.


## -see-also




<a href="https://msdn.microsoft.com/82fee86a-8704-4f22-8f11-f89509c5a0aa">CryptExportPKCS8Ex</a>



<a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a>



<a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="https://msdn.microsoft.com/d3b2b942-bde5-4399-9412-95fe227cd546">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>
 

 

