---
UID: NF:certenroll.IX509SignatureInformation.put_PublicKeyAlgorithm
title: IX509SignatureInformation::put_PublicKeyAlgorithm (certenroll.h)
description: Specifies and retrieves an object identifier (OID) for the public key algorithm used in the GetSignatureAlgorithm method. (Put)
helpviewer_keywords: ["IX509SignatureInformation interface [Security]","PublicKeyAlgorithm property","IX509SignatureInformation.PublicKeyAlgorithm","IX509SignatureInformation.put_PublicKeyAlgorithm","IX509SignatureInformation::PublicKeyAlgorithm","IX509SignatureInformation::get_PublicKeyAlgorithm","IX509SignatureInformation::put_PublicKeyAlgorithm","PublicKeyAlgorithm property [Security]","PublicKeyAlgorithm property [Security]","IX509SignatureInformation interface","certenroll/IX509SignatureInformation::PublicKeyAlgorithm","certenroll/IX509SignatureInformation::get_PublicKeyAlgorithm","certenroll/IX509SignatureInformation::put_PublicKeyAlgorithm","put_PublicKeyAlgorithm","security.ix509signatureinformation_publickeyalgorithm_property"]
old-location: security\ix509signatureinformation_publickeyalgorithm_property.htm
tech.root: security
ms.assetid: f964328f-15a6-4d8e-a2cf-73c8d74995e8
ms.date: 12/05/2018
ms.keywords: IX509SignatureInformation interface [Security],PublicKeyAlgorithm property, IX509SignatureInformation.PublicKeyAlgorithm, IX509SignatureInformation.put_PublicKeyAlgorithm, IX509SignatureInformation::PublicKeyAlgorithm, IX509SignatureInformation::get_PublicKeyAlgorithm, IX509SignatureInformation::put_PublicKeyAlgorithm, PublicKeyAlgorithm property [Security], PublicKeyAlgorithm property [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::PublicKeyAlgorithm, certenroll/IX509SignatureInformation::get_PublicKeyAlgorithm, certenroll/IX509SignatureInformation::put_PublicKeyAlgorithm, put_PublicKeyAlgorithm, security.ix509signatureinformation_publickeyalgorithm_property
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
 - IX509SignatureInformation::put_PublicKeyAlgorithm
 - certenroll/IX509SignatureInformation::put_PublicKeyAlgorithm
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
 - IX509SignatureInformation.PublicKeyAlgorithm
 - IX509SignatureInformation.get_PublicKeyAlgorithm
 - IX509SignatureInformation.put_PublicKeyAlgorithm
---

# IX509SignatureInformation::put_PublicKeyAlgorithm


## -description

The <b>PublicKeyAlgorithm</b> property specifies and retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the public key algorithm used in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method.

This property is read/write.

## -parameters

## -remarks

Unless you are retrieving a signature algorithm for a null-signed certificate request, you must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method. You must also set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm">HashAlgorithm</a> property. You can also set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a>   properties.

The <b>PublicKeyAlgorithm</b> property validates whether the OID you specify represents a public key algorithm. If the OID is valid, the property also clears the signature property cache.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
