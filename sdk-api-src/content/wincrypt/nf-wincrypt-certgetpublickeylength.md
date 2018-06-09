---
UID: NF:wincrypt.CertGetPublicKeyLength
title: CertGetPublicKeyLength function
author: windows-sdk-content
description: The CertGetPublicKeyLength function acquires the bit length of public/private keys from a public key BLOB.
old-location: security\certgetpublickeylength.htm
old-project: SecCrypto
ms.assetid: e67923f4-cd1f-4952-88f1-92ee26423f87
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CertGetPublicKeyLength, CertGetPublicKeyLength function [Security], _crypto2_certgetpublickeylength, security.certgetpublickeylength, wincrypt/CertGetPublicKeyLength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetPublicKeyLength
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertGetPublicKeyLength function


## -description



			The <b>CertGetPublicKeyLength</b> function acquires the bit length of public/private keys from a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a>.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pPublicKey [in]

A pointer to the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a> containing the keys for which the length is being retrieved.


## -returns




						Returns the length of the public/private keys in bits. If unable to determine the key's length, returns zero.

Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to see the reason for any failures.




## -see-also




<a href="https://www.bing.com/search?q=Data+Management+Functions">Data Management Functions</a>
 

 

