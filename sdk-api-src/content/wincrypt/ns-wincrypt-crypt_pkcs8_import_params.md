---
UID: NS:wincrypt._CRYPT_PKCS8_IMPORT_PARAMS
title: CRYPT_PKCS8_IMPORT_PARAMS
author: windows-sdk-content
description: Contains a PKCS #8 private key and pointers to callback functions. CRYPT_PKCS8_IMPORT_PARAMS is used by the CryptImportPKCS8 function.
old-location: security\crypt_pkcs8_import_params.htm
tech.root: seccrypto
ms.assetid: a016e807-60d3-4ae4-829b-43acea2ee8c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCRYPT_PKCS8_IMPORT_PARAMS, *PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, CRYPT_PKCS8_IMPORT_PARAMS, CRYPT_PKCS8_IMPORT_PARAMS structure [Security], CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure [Security], PCRYPT_PKCS8_IMPORT_PARAMS, PCRYPT_PKCS8_IMPORT_PARAMS structure pointer [Security], PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure pointer [Security], security.crypt_pkcs8_import_params, wincrypt/CRYPT_PKCS8_IMPORT_PARAMS, wincrypt/CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, wincrypt/PCRYPT_PKCS8_IMPORT_PARAMS, wincrypt/PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
 - CRYPT_PKCS8_IMPORT_PARAMS
product: Windows
targetos: Windows
req.typenames: CRYPT_PKCS8_IMPORT_PARAMS, *PCRYPT_PKCS8_IMPORT_PARAMS, CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, *PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS
req.redist: 
---

# CRYPT_PKCS8_IMPORT_PARAMS structure


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
 

 

