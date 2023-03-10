---
UID: NF:certenroll.IX509SignatureInformation.get_AlternateSignatureAlgorithmSet
title: IX509SignatureInformation::get_AlternateSignatureAlgorithmSet (certenroll.h)
description: Retrieves a Boolean value that specifies whether the AlternateSignatureAlgorithm property has been explicitly set by a caller.
helpviewer_keywords: ["AlternateSignatureAlgorithmSet property [Security]","AlternateSignatureAlgorithmSet property [Security]","IX509SignatureInformation interface","IX509SignatureInformation interface [Security]","AlternateSignatureAlgorithmSet property","IX509SignatureInformation.AlternateSignatureAlgorithmSet","IX509SignatureInformation.get_AlternateSignatureAlgorithmSet","IX509SignatureInformation::AlternateSignatureAlgorithmSet","IX509SignatureInformation::get_AlternateSignatureAlgorithmSet","certenroll/IX509SignatureInformation::AlternateSignatureAlgorithmSet","certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithmSet","get_AlternateSignatureAlgorithmSet","security.ix509signatureinformation_alternatesignaturealgorithmset_property"]
old-location: security\ix509signatureinformation_alternatesignaturealgorithmset_property.htm
tech.root: security
ms.assetid: fd28072f-9b79-4068-b4dd-61a6a4f8beda
ms.date: 12/05/2018
ms.keywords: AlternateSignatureAlgorithmSet property [Security], AlternateSignatureAlgorithmSet property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],AlternateSignatureAlgorithmSet property, IX509SignatureInformation.AlternateSignatureAlgorithmSet, IX509SignatureInformation.get_AlternateSignatureAlgorithmSet, IX509SignatureInformation::AlternateSignatureAlgorithmSet, IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::AlternateSignatureAlgorithmSet, certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithmSet, get_AlternateSignatureAlgorithmSet, security.ix509signatureinformation_alternatesignaturealgorithmset_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509SignatureInformation::get_AlternateSignatureAlgorithmSet
 - certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithmSet
dev_langs:
 - c++
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
---

# IX509SignatureInformation::get_AlternateSignatureAlgorithmSet


## -description

The <b>AlternateSignatureAlgorithmSet</b> property retrieves a Boolean value that specifies whether the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> property has been explicitly set by a caller.

This property is read-only.

## -parameters

## -remarks

The <b>AlternateSignatureAlgorithmSet</b> property is used by a CMC certificate request object. If the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> property is explicitly set on a signer certificate, and the same property is set on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object, the CMC request will not override the property value on the signer certificate.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>