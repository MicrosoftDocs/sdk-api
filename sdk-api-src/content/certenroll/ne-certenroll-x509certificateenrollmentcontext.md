---
UID: NE:certenroll.X509CertificateEnrollmentContext
title: X509CertificateEnrollmentContext (certenroll.h)
description: Specifies the nature of the end entity for which the certificate is intended.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","X509CertificateEnrollmentContext","X509CertificateEnrollmentContext enumeration [Security]","certenroll/ContextAdministratorForceMachine","certenroll/ContextMachine","certenroll/ContextUser","certenroll/X509CertificateEnrollmentContext","security.x509certificateenrollmentcontext_enum"]
old-location: security\x509certificateenrollmentcontext_enum.htm
tech.root: security
ms.assetid: 2db0e129-a566-47ba-ab57-53c7db09e8e3
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, X509CertificateEnrollmentContext, X509CertificateEnrollmentContext enumeration [Security], certenroll/ContextAdministratorForceMachine, certenroll/ContextMachine, certenroll/ContextUser, certenroll/X509CertificateEnrollmentContext, security.x509certificateenrollmentcontext_enum
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
req.typenames: X509CertificateEnrollmentContext
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509CertificateEnrollmentContext
 - certenroll/X509CertificateEnrollmentContext
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
 - X509CertificateEnrollmentContext
---

# X509CertificateEnrollmentContext enumeration


## -description

The <b>X509CertificateEnrollmentContext</b> enumeration  specifies the nature of the end entity for which the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> is intended. This enumeration is used by the following interfaces:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
</li>
</ul>

## -enum-fields

### -field ContextNone:0

### -field ContextUser:0x1

The certificate is intended for an end user.

### -field ContextMachine:0x2

The certificate is intended for a computer.

### -field ContextAdministratorForceMachine:0x3

The certificate is being requested by an administrator acting on the behalf of a computer.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>
