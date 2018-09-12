---
UID: NE:certenroll.EnrollmentTemplateProperty
title: EnrollmentTemplateProperty
author: windows-sdk-content
description: Contains property values for a given template.
old-location: security\enrollmenttemplateproperty.htm
tech.root: SecCertEnroll
ms.assetid: 408473d7-cfaa-4303-88f2-2a9d7dc6dc21
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnrollmentTemplateProperty, EnrollmentTemplateProperty enumeration [Security], TemplatePropAsymmetricAlgorithm, TemplatePropCertificatePolicies, TemplatePropCommonName, TemplatePropCryptoProviders, TemplatePropDescription, TemplatePropEKUs, TemplatePropEnrollmentFlags, TemplatePropExtensions, TemplatePropFriendlyName, TemplatePropGeneralFlags, TemplatePropHashAlgorithm, TemplatePropKeySecurityDescriptor, TemplatePropKeySpec, TemplatePropMajorRevision, TemplatePropMinimumKeySize, TemplatePropMinorRevision, TemplatePropOID, TemplatePropPrivateKeyFlags, TemplatePropRACertificatePolicies, TemplatePropRAEKUs, TemplatePropRASignatureCount, TemplatePropRenewalPeriod, TemplatePropSchemaVersion, TemplatePropSecurityDescriptor, TemplatePropSubjectNameFlags, TemplatePropSupersede, TemplatePropSymmetricAlgorithm, TemplatePropSymmetricKeyLength, TemplatePropV1ApplicationPolicy, TemplatePropValidityPeriod, certenroll/EnrollmentTemplateProperty, certenroll/TemplatePropAsymmetricAlgorithm, certenroll/TemplatePropCertificatePolicies, certenroll/TemplatePropCommonName, certenroll/TemplatePropCryptoProviders, certenroll/TemplatePropDescription, certenroll/TemplatePropEKUs, certenroll/TemplatePropEnrollmentFlags, certenroll/TemplatePropExtensions, certenroll/TemplatePropFriendlyName, certenroll/TemplatePropGeneralFlags, certenroll/TemplatePropHashAlgorithm, certenroll/TemplatePropKeySecurityDescriptor, certenroll/TemplatePropKeySpec, certenroll/TemplatePropMajorRevision, certenroll/TemplatePropMinimumKeySize, certenroll/TemplatePropMinorRevision, certenroll/TemplatePropOID, certenroll/TemplatePropPrivateKeyFlags, certenroll/TemplatePropRACertificatePolicies, certenroll/TemplatePropRAEKUs, certenroll/TemplatePropRASignatureCount, certenroll/TemplatePropRenewalPeriod, certenroll/TemplatePropSchemaVersion, certenroll/TemplatePropSecurityDescriptor, certenroll/TemplatePropSubjectNameFlags, certenroll/TemplatePropSupersede, certenroll/TemplatePropSymmetricAlgorithm, certenroll/TemplatePropSymmetricKeyLength, certenroll/TemplatePropV1ApplicationPolicy, certenroll/TemplatePropValidityPeriod, security.enrollmenttemplateproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Certenroll.h
api_name:
 - EnrollmentTemplateProperty
product: Windows
targetos: Windows
req.typenames: EnrollmentTemplateProperty
req.redist: 
---

# EnrollmentTemplateProperty enumeration


## -description


The <b>EnrollmentTemplateProperty</b> enumeration contains property values for a given template.


## -enum-fields




### -field TemplatePropCommonName

A <b>VT_BSTR</b> value that contains the common name of the template in Active Directory.


### -field TemplatePropFriendlyName

A <b>VT_BSTR</b> value that contains the template display name.


### -field TemplatePropEKUs

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that contains a collection of extended key usage object identifiers. This value applies to version 2 and later templates.


### -field TemplatePropCryptoProviders

A <b>VT_ARRAY|VT_BSTR</b> collection of cryptographic service providers (version 2) and key storage providers (version 3) that the client can use when generating requests based on  this template.


### -field TemplatePropMajorRevision

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the major version number for the template.


### -field TemplatePropDescription

Not used.


### -field TemplatePropKeySpec

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that contains <b>AT_SIGNATURE</b> or <b>AT_KEYEXCHANGE</b> to specify the <b>Key_Spec</b> value for legacy cryptographic service providers.


### -field TemplatePropSchemaVersion

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the template version. Currently, this can be 1, 2, or 3.


### -field TemplatePropMinorRevision

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the minor version number of a version 2 and later template.


### -field TemplatePropRASignatureCount

A <b>VT_UI4</b>  (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the number of recovery agent signatures that are required when generating a certificate request base on this template.


### -field TemplatePropMinimumKeySize

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the minimum size of the public key used by the enrolling client.


### -field TemplatePropOID

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that contains an object identifier for this template. This value applies to version 2 and later templates.


### -field TemplatePropSupersede

A <b>VT_ARRAY|VT_BSTR</b> collection that contains the common names of all version 2 and later templates that have been superseded.


### -field TemplatePropRACertificatePolicies

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that contains a collection of certificate policy object identifiers for the registration authority certificates. This value applies to version 2 and later templates.


### -field TemplatePropRAEKUs

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that contains a collection of application policy object identifiers for the registration authority certificates. This value applies to version 2 and later templates.


### -field TemplatePropCertificatePolicies

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that contains a collection of policy object identifiers to be added to the certificate policy extension.


### -field TemplatePropV1ApplicationPolicy

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that contains a collection of policy object identifiers to be added to the certificate application policy extension.


### -field TemplatePropAsymmetricAlgorithm

A <b>VT_BSTR</b> value that specifies the name of a public key algorithm the enrolling client must use when generating a certificate request based on  this template. This value applies to version 3 and later templates.


### -field TemplatePropKeySecurityDescriptor

A <b>VT_BSTR</b> value that specifies the asymmetric key security descriptor for version 3 and later templates.


### -field TemplatePropSymmetricAlgorithm

A <b>VT_BSTR</b> value that specifies the name of the symmetric algorithm that a client must use for key exchange when using this template. This value applies to version 3 and later templates.


### -field TemplatePropSymmetricKeyLength

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that specifies the length, in bits, of the symmetric key. This value applies to version 3 and later templates.


### -field TemplatePropHashAlgorithm

A <b>VT_BSTR</b> value that specifies the name of the hashing algorithm that an enrolling client must use. This value applies to version 3 and later templates.


### -field TemplatePropKeyUsage


### -field TemplatePropEnrollmentFlags

A <b>VT_I4</b> value that contains a bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/eefb2120-637d-45ae-91be-e18a9d9cb14f">X509CertificateTemplateEnrollmentFlag</a> values.


### -field TemplatePropSubjectNameFlags

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that contains a bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/0880bb94-d26f-49a7-9749-f8be272fa4f6">X509CertificateTemplateSubjectNameFlag</a> values.


### -field TemplatePropPrivateKeyFlags

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that contains a bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/b908b5fb-9089-493d-9ef4-1fe429ec43d4">X509CertificateTemplatePrivateKeyFlag</a> values.


### -field TemplatePropGeneralFlags

A <b>VT_UI4</b> (<b>VT_I4</b> beginning with Windows 8.1) value that contains a bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/0211dd53-39b7-49fb-8acd-e4d02a226904">X509CertificateTemplateGeneralFlag</a> values.


### -field TemplatePropSecurityDescriptor

A <b>VT_BSTR</b> value that specifies the security descriptor.


### -field TemplatePropExtensions

A <b>VT_DISPATCH</b> pointer to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> interface that contains the certificate extensions to be added to the certificate request when generating requests based on this template.


### -field TemplatePropValidityPeriod

A <b>VT_UI8 FILETIME</b> value that contains the maximum validity period, in seconds, of the certificate.


### -field TemplatePropRenewalPeriod

A <b>VT_UI8 FILETIME</b> value that specifies the amount of time before expiration that automatic enrollment has to  attempt certificate renewal.

