---
UID: NE:certenroll.X509KeySpec
title: X509KeySpec
author: windows-sdk-content
description: Specifies the intended use of a key for a legacy cryptographic service provider (CSP).
old-location: security\x509keyspec_enum.htm
old-project: seccertenroll
ms.assetid: d677d46c-3b36-4081-a6db-123ac1cef84b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: X509KeySpec, X509KeySpec enumeration [Security], XCN_AT_KEYEXCHANGE, XCN_AT_NONE, XCN_AT_SIGNATURE, certenroll/X509KeySpec, certenroll/XCN_AT_KEYEXCHANGE, certenroll/XCN_AT_NONE, certenroll/XCN_AT_SIGNATURE, security.x509keyspec_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509KeySpec
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509KeySpec enumeration


## -description


The <b>X509KeySpec</b> enumeration type specifies the intended use of a key for a legacy <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP). Legacy CSPs can support at most one signature algorithm (XCN_AT_SIGNATURE) and one encryption algorithm (XCN_AT_KEYEXCHANGE). This enumeration is used by the following interfaces:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
</li>
</ul>



## -enum-fields




### -field XCN_AT_NONE

The intended use is not identified. This value is set if the provider that supports the key is a  Cryptography API: Next Generation (CNG) key storage provider (KSP). 


### -field XCN_AT_KEYEXCHANGE

The key can be used to encrypt (including key exchange) or sign depending on the algorithm. For RSA algorithms, if this value is set, the key can be used for both signing and encryption. For other algorithms, signing may not be supported. Further, only encryption for key exchange may be supported.

<div class="alert"><b>Note</b>  The KEYEXCHANGE portion of the value name is a carryover from CryptoAPI where it originally  referred to the symmetric encryption of a <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> used during key exchange. Use of the term ultimately expanded to cover all symmetric encryption.</div>
<div> </div>

### -field XCN_AT_SIGNATURE

The key can be used for signing.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

