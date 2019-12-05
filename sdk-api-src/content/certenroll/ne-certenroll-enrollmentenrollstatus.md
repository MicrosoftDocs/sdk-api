---
UID: NE:certenroll.EnrollmentEnrollStatus
title: EnrollmentEnrollStatus (certenroll.h)
description: Specifies the enrollment status of a certificate request.
old-location: security\enrollmentenrollstatus_enum.htm
tech.root: seccertenroll
ms.assetid: ed27cc77-7ff2-4f22-87c4-c6edc0709813
ms.date: 12/05/2018
ms.keywords: EnrollDenied, EnrollError, EnrollPended, EnrollSkipped, EnrollUIDeferredEnrollmentRequired, EnrollUnknown, Enrolled, EnrollmentEnrollStatus, EnrollmentEnrollStatus enumeration [Security], certenroll/EnrollDenied, certenroll/EnrollError, certenroll/EnrollPended, certenroll/EnrollSkipped, certenroll/EnrollUIDeferredEnrollmentRequired, certenroll/EnrollUnknown, certenroll/Enrolled, certenroll/EnrollmentEnrollStatus, security.enrollmentenrollstatus_enum
ms.topic: enum
f1_keywords:
- certenroll/EnrollmentEnrollStatus
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- CertEnroll.h
api_name:
- EnrollmentEnrollStatus
targetos: Windows
req.typenames: EnrollmentEnrollStatus
req.redist: 
ms.custom: 19H1
---

# EnrollmentEnrollStatus enumeration


## -description


The <b>EnrollmentEnrollStatus</b> enumeration type specifies the enrollment status of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>. This enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_status">Status</a> property on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> interface.


## -enum-fields




### -field Enrolled

The enrollment succeeded, and the certificate has been issued.


### -field EnrollPended

The request has been submitted and the enrollment is pending, or the request has been issued out of band.


### -field EnrollUIDeferredEnrollmentRequired

Enrollment must be deferred.


### -field EnrollError

An error occurred.


### -field EnrollUnknown

The enrollment status is unknown.


### -field EnrollSkipped

The status information has been skipped. This can occur if a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> is not valid or has not been selected for monitoring.


### -field EnrollDenied

Enrollment has been denied.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-enrollmentselectionstatus">EnrollmentSelectionStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
 

 

