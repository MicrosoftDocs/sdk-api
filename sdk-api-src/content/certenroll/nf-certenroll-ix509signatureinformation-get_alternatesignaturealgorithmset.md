---
UID: NF:certenroll.IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
title: IX509SignatureInformation::get_AlternateSignatureAlgorithmSet
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether the AlternateSignatureAlgorithm property has been explicitly set by a caller.
old-location: security\ix509signatureinformation_alternatesignaturealgorithmset_property.htm
tech.root: SecCertEnroll
ms.assetid: fd28072f-9b79-4068-b4dd-61a6a4f8beda
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AlternateSignatureAlgorithmSet property [Security], AlternateSignatureAlgorithmSet property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],AlternateSignatureAlgorithmSet property, IX509SignatureInformation.AlternateSignatureAlgorithmSet, IX509SignatureInformation.get_AlternateSignatureAlgorithmSet, IX509SignatureInformation::AlternateSignatureAlgorithmSet, IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, get_AlternateSignatureAlgorithmSet, security.ix509signatureinformation_alternatesignaturealgorithmset_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509SignatureInformation.AlternateSignatureAlgorithmSet
 - IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
: 
---

# IX509SignatureInformation::get_AlternateSignatureAlgorithmSet


## -description


The <b>AlternateSignatureAlgorithmSet</b> property retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/en-us/library/Aa965846(v=VS.85).aspx">AlternateSignatureAlgorithm</a> property has been explicitly set by a caller.

This property is read-only.


## -parameters


## -remarks



The <b>AlternateSignatureAlgorithmSet</b> property is used by a CMC certificate request object. If the <a href="https://msdn.microsoft.com/en-us/library/Aa965846(v=VS.85).aspx">AlternateSignatureAlgorithm</a> property is explicitly set on a signer certificate, and the same property is set on the <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> object, the CMC request will not override the property value on the signer certificate.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

