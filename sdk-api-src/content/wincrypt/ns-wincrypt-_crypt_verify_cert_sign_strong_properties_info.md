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

# _CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure


## -description


Contains the length, in bits, of the public key and the  names of the signing and hashing algorithms used for strong signing.


## -struct-fields




### -field CertSignHashCNGAlgPropData

The buffer contains a Unicode string that denotes the signing algorithm / hashing algorithm pair used, for example "RSA/SHA256". 


### -field CertIssuerPubKeyBitLengthPropData

The buffer contains the length, in bits, of the asymmetric key used for signing.


## -remarks



This structure is returned by the <a href="https://msdn.microsoft.com/8a84af66-b174-4a3e-b1d7-6f218a52d877">CryptVerifyCertificateSignatureEx</a> function when the <i>dwFlags</i> parameter is set to <b>CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG</b>. 




## -see-also




<a href="https://msdn.microsoft.com/8a84af66-b174-4a3e-b1d7-6f218a52d877">CryptVerifyCertificateSignatureEx</a>
 

 

