---
UID: NF:certenroll.IX509SignatureInformation.put_NullSigned
title: IX509SignatureInformation::put_NullSigned (certenroll.h)
description: Specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed. (Put)
helpviewer_keywords: ["IX509SignatureInformation interface [Security]","NullSigned property","IX509SignatureInformation.NullSigned","IX509SignatureInformation.put_NullSigned","IX509SignatureInformation::NullSigned","IX509SignatureInformation::get_NullSigned","IX509SignatureInformation::put_NullSigned","NullSigned property [Security]","NullSigned property [Security]","IX509SignatureInformation interface","certenroll/IX509SignatureInformation::NullSigned","certenroll/IX509SignatureInformation::get_NullSigned","certenroll/IX509SignatureInformation::put_NullSigned","put_NullSigned","security.ix509signatureinformation_nullsigned_property"]
old-location: security\ix509signatureinformation_nullsigned_property.htm
tech.root: security
ms.assetid: a693343e-7c9a-4967-b46c-53936497662a
ms.date: 12/05/2018
ms.keywords: IX509SignatureInformation interface [Security],NullSigned property, IX509SignatureInformation.NullSigned, IX509SignatureInformation.put_NullSigned, IX509SignatureInformation::NullSigned, IX509SignatureInformation::get_NullSigned, IX509SignatureInformation::put_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::NullSigned, certenroll/IX509SignatureInformation::get_NullSigned, certenroll/IX509SignatureInformation::put_NullSigned, put_NullSigned, security.ix509signatureinformation_nullsigned_property
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
 - IX509SignatureInformation::put_NullSigned
 - certenroll/IX509SignatureInformation::put_NullSigned
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
 - IX509SignatureInformation.NullSigned
 - IX509SignatureInformation.get_NullSigned
 - IX509SignatureInformation.put_NullSigned
---

# IX509SignatureInformation::put_NullSigned


## -description

The <b>NullSigned</b> property specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed.

This property is read/write.

## -parameters

## -remarks

A null-signed certificate request is not really signed. That is, the request can be digested by using a digest algorithm such as SHA-1, but it is not encrypted with a public key algorithm such as RSA. You must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-getsignaturealgorithm">GetSignatureAlgorithm</a> method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
