---
UID: NF:certenroll.IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
title: IX509SignatureInformation::get_AlternateSignatureAlgorithmSet
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether the AlternateSignatureAlgorithm property has been explicitly set by a caller.
old-location: security\ix509signatureinformation_alternatesignaturealgorithmset_property.htm
old-project: SecCertEnroll
ms.assetid: fd28072f-9b79-4068-b4dd-61a6a4f8beda
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: AlternateSignatureAlgorithmSet property [Security], AlternateSignatureAlgorithmSet property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],AlternateSignatureAlgorithmSet property, IX509SignatureInformation.AlternateSignatureAlgorithmSet, IX509SignatureInformation.get_AlternateSignatureAlgorithmSet, IX509SignatureInformation::AlternateSignatureAlgorithmSet, IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, get_AlternateSignatureAlgorithmSet, security.ix509signatureinformation_alternatesignaturealgorithmset_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509SignatureInformation.AlternateSignatureAlgorithmSet
-	IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509SignatureInformation::get_AlternateSignatureAlgorithmSet


## -description


The <b>AlternateSignatureAlgorithmSet</b> property retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a> property has been explicitly set by a caller.

This property is read-only.


## -parameters


## -remarks



The <b>AlternateSignatureAlgorithmSet</b> property is used by a CMC certificate request object. If the <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a> property is explicitly set on a signer certificate, and the same property is set on the <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> object, the CMC request will not override the property value on the signer certificate.




## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

