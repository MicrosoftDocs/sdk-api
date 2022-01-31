---
UID: NE:certenroll.X509CertificateTemplateEnrollmentFlag
title: X509CertificateTemplateEnrollmentFlag (certenroll.h)
description: Contains values that specify server and client actions during enrollment.
helpviewer_keywords: ["EnrollmentAddOCSPNoCheck","EnrollmentAddTemplateName","EnrollmentAllowEnrollOnBehalfOf","EnrollmentAutoEnrollment","EnrollmentAutoEnrollmentCheckUserDSCertificate","EnrollmentDomainAuthenticationNotRequired","EnrollmentIncludeBasicConstraintsForEECerts","EnrollmentIncludeSymmetricAlgorithms","EnrollmentNoRevocationInfoInCerts","EnrollmentPendAllRequests","EnrollmentPreviousApprovalValidateReenrollment","EnrollmentPublishToDS","EnrollmentPublishToKRAContainer","EnrollmentRemoveInvalidCertificateFromPersonalStore","EnrollmentReuseKeyOnFullSmartCard","EnrollmentUserInteractionRequired","X509CertificateTemplateEnrollmentFlag","X509CertificateTemplateEnrollmentFlag enumeration [Security]","certenroll/EnrollmentAddOCSPNoCheck","certenroll/EnrollmentAddTemplateName","certenroll/EnrollmentAllowEnrollOnBehalfOf","certenroll/EnrollmentAutoEnrollment","certenroll/EnrollmentAutoEnrollmentCheckUserDSCertificate","certenroll/EnrollmentDomainAuthenticationNotRequired","certenroll/EnrollmentIncludeBasicConstraintsForEECerts","certenroll/EnrollmentIncludeSymmetricAlgorithms","certenroll/EnrollmentNoRevocationInfoInCerts","certenroll/EnrollmentPendAllRequests","certenroll/EnrollmentPreviousApprovalValidateReenrollment","certenroll/EnrollmentPublishToDS","certenroll/EnrollmentPublishToKRAContainer","certenroll/EnrollmentRemoveInvalidCertificateFromPersonalStore","certenroll/EnrollmentReuseKeyOnFullSmartCard","certenroll/EnrollmentUserInteractionRequired","certenroll/X509CertificateTemplateEnrollmentFlag","security.x509certificatetemplateenrollmentflag"]
old-location: security\x509certificatetemplateenrollmentflag.htm
tech.root: security
ms.assetid: eefb2120-637d-45ae-91be-e18a9d9cb14f
ms.date: 12/05/2018
ms.keywords: EnrollmentAddOCSPNoCheck, EnrollmentAddTemplateName, EnrollmentAllowEnrollOnBehalfOf, EnrollmentAutoEnrollment, EnrollmentAutoEnrollmentCheckUserDSCertificate, EnrollmentDomainAuthenticationNotRequired, EnrollmentIncludeBasicConstraintsForEECerts, EnrollmentIncludeSymmetricAlgorithms, EnrollmentNoRevocationInfoInCerts, EnrollmentPendAllRequests, EnrollmentPreviousApprovalValidateReenrollment, EnrollmentPublishToDS, EnrollmentPublishToKRAContainer, EnrollmentRemoveInvalidCertificateFromPersonalStore, EnrollmentReuseKeyOnFullSmartCard, EnrollmentUserInteractionRequired, X509CertificateTemplateEnrollmentFlag, X509CertificateTemplateEnrollmentFlag enumeration [Security], certenroll/EnrollmentAddOCSPNoCheck, certenroll/EnrollmentAddTemplateName, certenroll/EnrollmentAllowEnrollOnBehalfOf, certenroll/EnrollmentAutoEnrollment, certenroll/EnrollmentAutoEnrollmentCheckUserDSCertificate, certenroll/EnrollmentDomainAuthenticationNotRequired, certenroll/EnrollmentIncludeBasicConstraintsForEECerts, certenroll/EnrollmentIncludeSymmetricAlgorithms, certenroll/EnrollmentNoRevocationInfoInCerts, certenroll/EnrollmentPendAllRequests, certenroll/EnrollmentPreviousApprovalValidateReenrollment, certenroll/EnrollmentPublishToDS, certenroll/EnrollmentPublishToKRAContainer, certenroll/EnrollmentRemoveInvalidCertificateFromPersonalStore, certenroll/EnrollmentReuseKeyOnFullSmartCard, certenroll/EnrollmentUserInteractionRequired, certenroll/X509CertificateTemplateEnrollmentFlag, security.x509certificatetemplateenrollmentflag
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
targetos: Windows
req.typenames: X509CertificateTemplateEnrollmentFlag
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509CertificateTemplateEnrollmentFlag
 - certenroll/X509CertificateTemplateEnrollmentFlag
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
 - X509CertificateTemplateEnrollmentFlag
---

# X509CertificateTemplateEnrollmentFlag enumeration


## -description

The <b>X509CertificateTemplateEnrollmentFlag</b> enumeration contains values that specify server and client actions during enrollment.

## -enum-fields

### -field EnrollmentIncludeSymmetricAlgorithms:0x1

Instructs the client and server to include a Secure/Multipurpose Internet Mail Extensions (S/MIME) extension in the certificate request and issued certificate.

### -field EnrollmentPendAllRequests:0x2

Instructs the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) to place all certificate requests in a pending state.

### -field EnrollmentPublishToKRAContainer:0x4

Instructs the certification authority to publish the issued certificate to the key recovery agent (KRA) container in Active Directory.

### -field EnrollmentPublishToDS:0x8

Instructs clients and servers to append the issued certificate to the <b>userCertificate</b> attribute on the user object in Active Directory.

### -field EnrollmentAutoEnrollmentCheckUserDSCertificate:0x10

Instructs clients to not automatically enroll a certificate based on this template if the <b>userCertificate</b> attribute on the user object in Active Directory already contains a valid certificate based on this template.

### -field EnrollmentAutoEnrollment:0x20

Instructs clients to automatically enroll a certificate that is based on this template.

### -field EnrollmentDomainAuthenticationNotRequired:0x80

Not used.

### -field EnrollmentPreviousApprovalValidateReenrollment:0x40

Instructs clients to sign a certificate by using private keys whose public keys are contained in  existing certificates.

### -field EnrollmentUserInteractionRequired:0x100

Instructs the client to obtain user consent before attempting to enroll a certificate request based on this template.

### -field EnrollmentAddTemplateName:0x200

Not used.

### -field EnrollmentRemoveInvalidCertificateFromPersonalStore:0x400

Instructs the client to delete expired, revoked, or renewed certificates from the local certificate store.

### -field EnrollmentAllowEnrollOnBehalfOf:0x800

Instructs the server to allow enroll-on-behalf-of (EOBO) functionality.

### -field EnrollmentAddOCSPNoCheck:0x1000

Instructs the server to not include revocation information in the issued certificate, adding instead an id-pkix-ocsp-nocheck extension that specifies that the certificate holder can be trusted for the life of the certificate.

### -field EnrollmentReuseKeyOnFullSmartCard:0x2000

Instructs the client to reuse a private key for a smart card based certificate renewal if a new private key cannot be created on the card.

### -field EnrollmentNoRevocationInfoInCerts:0x4000

Instructs the server to not include revocation information in the issued certificate.

### -field EnrollmentIncludeBasicConstraintsForEECerts:0x8000

Instructs the server to include the Basic Constraints extension in the issued certificate.

### -field EnrollmentPreviousApprovalKeyBasedValidateReenrollment:0x10000

### -field EnrollmentCertificateIssuancePoliciesFromRequest:0x20000

### -field EnrollmentSkipAutoRenewal:0x40000
