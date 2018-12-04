---
UID: NE:certenroll.KeyIdentifierHashAlgorithm
title: KeyIdentifierHashAlgorithm
author: windows-sdk-content
description: Specifies the algorithm used to hash the public key in a certificate request.
old-location: security\keyidentifierhashalgorithm_enum.htm
tech.root: seccertenroll
ms.assetid: 80e3c730-880f-4cfa-921f-3bb88cf827f2
ms.author: windowssdkdev
ms.date: 11/16/2018
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


The <b>KeyIdentifierHashAlgorithm</b> enumeration type specifies the algorithm used to <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This enumeration is used by the  <a href="https://msdn.microsoft.com/b2e471c7-1087-46a2-8938-5d3cea44f7f7">ComputeKeyIdentifier</a> method on the <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> interface, and the key identifier can be used to initialize the  <a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a> and <a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>  objects.


## -enum-fields




### -field SKIHashDefault

The default hash algorithm. This is redundant with the <b>SKIHashSha1</b> value.


### -field SKIHashSha1

A 160-bit SHA-1 hash of a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded public key, excluding the tag, length, and number of unused bits.


### -field SKIHashCapiSha1

A 160-bit SHA-1 hash of a DER-encoded public key, including the tag, length, and number of unused bits.


### -field SKIHashSha256

A 256-bit SHA256 (SHA-2) hash of a DER-encoded public key, including the tag, length, and number of unused bits.


### -field SKIHashHPKP




## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/b2e471c7-1087-46a2-8938-5d3cea44f7f7">ComputeKeyIdentifier</a>



<a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>



<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>



<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

