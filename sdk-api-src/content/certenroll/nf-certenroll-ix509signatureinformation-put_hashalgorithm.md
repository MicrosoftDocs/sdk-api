---
UID: NF:certenroll.IX509SignatureInformation.put_HashAlgorithm
title: IX509SignatureInformation::put_HashAlgorithm (certenroll.h)
description: Specifies and retrieves an object identifier (OID) for the hashing algorithm used in the GetSignatureAlgorithm method. (Put)
helpviewer_keywords: ["HashAlgorithm property [Security]","HashAlgorithm property [Security]","IX509SignatureInformation interface","IX509SignatureInformation interface [Security]","HashAlgorithm property","IX509SignatureInformation.HashAlgorithm","IX509SignatureInformation.put_HashAlgorithm","IX509SignatureInformation::HashAlgorithm","IX509SignatureInformation::get_HashAlgorithm","IX509SignatureInformation::put_HashAlgorithm","certenroll/IX509SignatureInformation::HashAlgorithm","certenroll/IX509SignatureInformation::get_HashAlgorithm","certenroll/IX509SignatureInformation::put_HashAlgorithm","put_HashAlgorithm","security.ix509signatureinformation_hashalgorithm_property"]
old-location: security\ix509signatureinformation_hashalgorithm_property.htm
tech.root: security
ms.assetid: b5242975-50e5-49d6-be1f-3a09ada03593
ms.date: 12/05/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],HashAlgorithm property, IX509SignatureInformation.HashAlgorithm, IX509SignatureInformation.put_HashAlgorithm, IX509SignatureInformation::HashAlgorithm, IX509SignatureInformation::get_HashAlgorithm, IX509SignatureInformation::put_HashAlgorithm, certenroll/IX509SignatureInformation::HashAlgorithm, certenroll/IX509SignatureInformation::get_HashAlgorithm, certenroll/IX509SignatureInformation::put_HashAlgorithm, put_HashAlgorithm, security.ix509signatureinformation_hashalgorithm_property
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
 - IX509SignatureInformation::put_HashAlgorithm
 - certenroll/IX509SignatureInformation::put_HashAlgorithm
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
 - IX509SignatureInformation.HashAlgorithm
 - IX509SignatureInformation.get_HashAlgorithm
 - IX509SignatureInformation.put_HashAlgorithm
---

# IX509SignatureInformation::put_HashAlgorithm


## -description

The <b>HashAlgorithm</b> property specifies and retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the hashing algorithm used in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method.

This property is read/write.

## -parameters

## -remarks

You must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method. You must also set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> property unless you are retrieving a signature algorithm for a null-signed certificate request.  You can also set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a>, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a>,  and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_parameters">Parameters</a> properties.

The <b>HashAlgorithm</b> property validates whether the OID you specify represents a hashing algorithm. If the OID is valid, the property also clears the signature property cache.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
