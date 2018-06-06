---
UID: NS:wincrypt._CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
title: "_CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO"
author: windows-sdk-content
description: Contains the length, in bits, of the public key and the names of the signing and hashing algorithms used for strong signing.
old-location: security\crypt_verify_cert_sign_strong_properties_info.htm
old-project: SecCrypto
ms.assetid: 7D68DE3D-B05D-4E06-9BA1-72E407E5FED2
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure [Security], PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure pointer [Security], _CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, security.crypt_verify_cert_sign_strong_properties_info, wincrypt/CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, wincrypt/PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, *PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

