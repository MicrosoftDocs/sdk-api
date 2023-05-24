---
UID: NF:certenroll.IX509SignatureInformation.put_AlternateSignatureAlgorithm
title: IX509SignatureInformation::put_AlternateSignatureAlgorithm (certenroll.h)
description: Specifies and retrieves a Boolean value that specifies whether the GetSignatureAlgorithm method should retrieve a discrete or combined algorithm object identifier (OID) for a PKCS (Put)
helpviewer_keywords: ["AlternateSignatureAlgorithm property [Security]","AlternateSignatureAlgorithm property [Security]","IX509SignatureInformation interface","IX509SignatureInformation interface [Security]","AlternateSignatureAlgorithm property","IX509SignatureInformation.AlternateSignatureAlgorithm","IX509SignatureInformation.put_AlternateSignatureAlgorithm","IX509SignatureInformation::AlternateSignatureAlgorithm","IX509SignatureInformation::get_AlternateSignatureAlgorithm","IX509SignatureInformation::put_AlternateSignatureAlgorithm","certenroll/IX509SignatureInformation::AlternateSignatureAlgorithm","certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithm","certenroll/IX509SignatureInformation::put_AlternateSignatureAlgorithm","put_AlternateSignatureAlgorithm","security.ix509signatureinformation_alternatesignaturealgorithm_property"]
old-location: security\ix509signatureinformation_alternatesignaturealgorithm_property.htm
tech.root: security
ms.assetid: e62ecdf1-56d8-4707-8e5d-deef4d79a34c
ms.date: 12/05/2018
ms.keywords: AlternateSignatureAlgorithm property [Security], AlternateSignatureAlgorithm property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],AlternateSignatureAlgorithm property, IX509SignatureInformation.AlternateSignatureAlgorithm, IX509SignatureInformation.put_AlternateSignatureAlgorithm, IX509SignatureInformation::AlternateSignatureAlgorithm, IX509SignatureInformation::get_AlternateSignatureAlgorithm, IX509SignatureInformation::put_AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::put_AlternateSignatureAlgorithm, put_AlternateSignatureAlgorithm, security.ix509signatureinformation_alternatesignaturealgorithm_property
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
 - IX509SignatureInformation::put_AlternateSignatureAlgorithm
 - certenroll/IX509SignatureInformation::put_AlternateSignatureAlgorithm
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
 - IX509SignatureInformation.AlternateSignatureAlgorithm
 - IX509SignatureInformation.get_AlternateSignatureAlgorithm
 - IX509SignatureInformation.put_AlternateSignatureAlgorithm
---

# IX509SignatureInformation::put_AlternateSignatureAlgorithm


## -description

The <b>AlternateSignatureAlgorithm</b> property specifies and retrieves a Boolean value that specifies whether the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method should retrieve a discrete or combined algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for a PKCS #10 certificate request.

This property is read/write.

## -parameters

## -remarks

PKCS #7 and CMC certificate requests always use a discrete signature algorithm OID and a separate hashing algorithm OID. Only PKCS #10 certificate requests use combined algorithm OIDs. You can set the <b>AlternateSignatureAlgorithm</b> property to retrieve a discrete signature algorithm OID from the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method for a PKCS #10 request. If you set this property, the hashing algorithm OID can be retrieved from the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_parameters">Parameters</a> property, and the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithmset">AlternateSignatureAlgorithmSet</a> property is also set. For examples of discrete and combined OIDs, see <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
