---
UID: NE:certenroll.X509KeySpec
title: X509KeySpec
author: windows-sdk-content
description: Specifies the intended use of a key for a legacy cryptographic service provider (CSP).
old-location: security\x509keyspec_enum.htm
tech.root: seccertenroll
ms.assetid: d677d46c-3b36-4081-a6db-123ac1cef84b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: X509KeySpec, X509KeySpec enumeration [Security], XCN_AT_KEYEXCHANGE, XCN_AT_NONE, XCN_AT_SIGNATURE, certenroll/X509KeySpec, certenroll/XCN_AT_KEYEXCHANGE, certenroll/XCN_AT_NONE, certenroll/XCN_AT_SIGNATURE, security.x509keyspec_enum
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CertEnroll.h
api_name:
 - X509KeySpec
product: Windows
targetos: Windows
req.typenames: X509KeySpec
req.redist: 
---

# X509KeySpec enumeration


## -description


The <b>X509KeySpec</b> enumeration type specifies the intended use of a key for a legacy <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). Legacy CSPs can support at most one signature algorithm (XCN_AT_SIGNATURE) and one encryption algorithm (XCN_AT_KEYEXCHANGE). This enumeration is used by the following interfaces:<ul>
<li>
<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
</li>
</ul>



## -enum-fields




### -field XCN_AT_NONE

The intended use is not identified. This value is set if the provider that supports the key is a  Cryptography API: Next Generation (CNG) key storage provider (KSP). 


### -field XCN_AT_KEYEXCHANGE

The key can be used to encrypt (including key exchange) or sign depending on the algorithm. For RSA algorithms, if this value is set, the key can be used for both signing and encryption. For other algorithms, signing may not be supported. Further, only encryption for key exchange may be supported.

<div class="alert"><b>Note</b>  The KEYEXCHANGE portion of the value name is a carryover from CryptoAPI where it originally  referred to the symmetric encryption of a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> used during key exchange. Use of the term ultimately expanded to cover all symmetric encryption.</div>
<div> </div>

### -field XCN_AT_SIGNATURE

The key can be used for signing.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

