---
UID: NE:certenroll.KeyIdentifierHashAlgorithm
title: KeyIdentifierHashAlgorithm
author: windows-sdk-content
description: Specifies the algorithm used to hash the public key in a certificate request.
old-location: security\keyidentifierhashalgorithm_enum.htm
tech.root: SecCertEnroll
ms.assetid: 80e3c730-880f-4cfa-921f-3bb88cf827f2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: KeyIdentifierHashAlgorithm, KeyIdentifierHashAlgorithm enumeration [Security], SKIHashCapiSha1, SKIHashDefault, SKIHashSha1, SKIHashSha256, certenroll/KeyIdentifierHashAlgorithm, certenroll/SKIHashCapiSha1, certenroll/SKIHashDefault, certenroll/SKIHashSha1, certenroll/SKIHashSha256, security.keyidentifierhashalgorithm_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - KeyIdentifierHashAlgorithm
product: Windows
targetos: Windows
req.typenames: KeyIdentifierHashAlgorithm
req.redist: 
---

# KeyIdentifierHashAlgorithm enumeration


## -description


The <b>KeyIdentifierHashAlgorithm</b> enumeration type specifies the algorithm used to <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a> the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> in a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>. This enumeration is used by the  <a href="https://msdn.microsoft.com/en-us/library/Aa379041(v=VS.85).aspx">ComputeKeyIdentifier</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa379039(v=VS.85).aspx">IX509PublicKey</a> interface, and the key identifier can be used to initialize the  <a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>  objects.


## -enum-fields




### -field SKIHashDefault

The default hash algorithm. This is redundant with the <b>SKIHashSha1</b> value.


### -field SKIHashSha1

A 160-bit SHA-1 hash of a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded public key, excluding the tag, length, and number of unused bits.


### -field SKIHashCapiSha1

A 160-bit SHA-1 hash of a DER-encoded public key, including the tag, length, and number of unused bits.


### -field SKIHashSha256

A 256-bit SHA256 (SHA-2) hash of a DER-encoded public key, including the tag, length, and number of unused bits.


### -field SKIHashHPKP




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379041(v=VS.85).aspx">ComputeKeyIdentifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379039(v=VS.85).aspx">IX509PublicKey</a>
 

 

