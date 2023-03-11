---
UID: NE:certenroll.PolicyQualifierType
title: PolicyQualifierType (certenroll.h)
description: Specifies the type of qualifier applied to a certificate policy.
helpviewer_keywords: ["PolicyQualifierType","PolicyQualifierType enumeration [Security]","PolicyQualifierTypeUnknown","PolicyQualifierTypeUrl","PolicyQualifierTypeUserNotice","certenroll/PolicyQualifierType","certenroll/PolicyQualifierTypeUnknown","certenroll/PolicyQualifierTypeUrl","certenroll/PolicyQualifierTypeUserNotice","security.policyqualifiertype_enum"]
old-location: security\policyqualifiertype_enum.htm
tech.root: security
ms.assetid: 76cd1874-b80d-466e-9c7d-12cf8d310b8a
ms.date: 12/05/2018
ms.keywords: PolicyQualifierType, PolicyQualifierType enumeration [Security], PolicyQualifierTypeUnknown, PolicyQualifierTypeUrl, PolicyQualifierTypeUserNotice, certenroll/PolicyQualifierType, certenroll/PolicyQualifierTypeUnknown, certenroll/PolicyQualifierTypeUrl, certenroll/PolicyQualifierTypeUserNotice, security.policyqualifiertype_enum
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
targetos: Windows
req.typenames: PolicyQualifierType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PolicyQualifierType
 - certenroll/PolicyQualifierType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - PolicyQualifierType
---

# PolicyQualifierType enumeration


## -description

The <b>PolicyQualifierType</b> enumeration type specifies the type of qualifier applied to a <a href="/windows/desktop/SecGloss/c-gly">certificate policy</a>. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> method and the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_type">Type</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> interface.

## -enum-fields

### -field PolicyQualifierTypeUnknown:0

The qualifier type is not specified.

### -field PolicyQualifierTypeUrl:1

The qualifier is a URL that points to a Certification Practice Statement (CPS) that has been defined by the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> to outline the policies under which the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> was issued and the purposes for which the certificate can be used.

### -field PolicyQualifierTypeUserNotice:2

The qualifier is a text statement to be displayed by the application to any user who relies on the certificate. The user notice identifies the permitted uses of the certificate.

### -field PolicyQualifierTypeFlags:3

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>
