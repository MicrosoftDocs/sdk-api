---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# X509CertificateTemplateEnrollmentFlag enumeration


## -description


The <b>X509CertificateTemplateEnrollmentFlag</b> enumeration contains values that specify server and client actions during enrollment.


## -enum-fields




### -field EnrollmentIncludeSymmetricAlgorithms

Instructs the client and server to include a Secure/Multipurpose Internet Mail Extensions (S/MIME) extension in the certificate request and issued certificate.


### -field EnrollmentPendAllRequests

Instructs the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) to place all certificate requests in a pending state.


### -field EnrollmentPublishToKRAContainer

Instructs the certification authority to publish the issued certificate to the key recovery agent (KRA) container in Active Directory.


### -field EnrollmentPublishToDS

Instructs clients and servers to append the issued certificate to the <b>userCertificate</b> attribute on the user object in Active Directory.


### -field EnrollmentAutoEnrollmentCheckUserDSCertificate

Instructs clients to not automatically enroll a certificate based on this template if the <b>userCertificate</b> attribute on the user object in Active Directory already contains a valid certificate based on this template.


### -field EnrollmentAutoEnrollment

Instructs clients to automatically enroll a certificate that is based on this template.


### -field EnrollmentDomainAuthenticationNotRequired

Not used.


### -field EnrollmentPreviousApprovalValidateReenrollment

Instructs clients to sign a certificate by using private keys whose public keys are contained in  existing certificates.


### -field EnrollmentUserInteractionRequired

Instructs the client to obtain user consent before attempting to enroll a certificate request based on this template.


### -field EnrollmentAddTemplateName

Not used.


### -field EnrollmentRemoveInvalidCertificateFromPersonalStore

Instructs the client to delete expired, revoked, or renewed certificates from the local certificate store.


### -field EnrollmentAllowEnrollOnBehalfOf

Instructs the server to allow enroll-on-behalf-of (EOBO) functionality.


### -field EnrollmentAddOCSPNoCheck

Instructs the server to not include revocation information in the issued certificate, adding instead an id-pkix-ocsp-nocheck extension that specifies that the certificate holder can be trusted for the life of the certificate.


### -field EnrollmentReuseKeyOnFullSmartCard

Instructs the client to reuse a private key for a smart card based certificate renewal if a new private key cannot be created on the card.


### -field EnrollmentNoRevocationInfoInCerts

Instructs the server to not include revocation information in the issued certificate.


### -field EnrollmentIncludeBasicConstraintsForEECerts

Instructs the server to include the Basic Constraints extension in the issued certificate.


### -field EnrollmentPreviousApprovalKeyBasedValidateReenrollment


### -field EnrollmentCertificateIssuancePoliciesFromRequest


### -field EnrollmentSkipAutoRenewal



