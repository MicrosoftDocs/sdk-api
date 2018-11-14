---
UID: NE:certenroll.EnrollmentEnrollStatus
title: EnrollmentEnrollStatus
author: windows-sdk-content
description: Specifies the enrollment status of a certificate request.
old-location: security\enrollmentenrollstatus_enum.htm
tech.root: SecCertEnroll
ms.assetid: ed27cc77-7ff2-4f22-87c4-c6edc0709813
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnrollDenied, EnrollError, EnrollPended, EnrollSkipped, EnrollUIDeferredEnrollmentRequired, EnrollUnknown, Enrolled, EnrollmentEnrollStatus, EnrollmentEnrollStatus enumeration [Security], certenroll/EnrollDenied, certenroll/EnrollError, certenroll/EnrollPended, certenroll/EnrollSkipped, certenroll/EnrollUIDeferredEnrollmentRequired, certenroll/EnrollUnknown, certenroll/Enrolled, certenroll/EnrollmentEnrollStatus, security.enrollmentenrollstatus_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: EnrollmentEnrollStatus
req.redist: 
---

# EnrollmentEnrollStatus enumeration


## -description


The <b>EnrollmentEnrollStatus</b> enumeration type specifies the enrollment status of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This enumeration is used by the <a href="https://msdn.microsoft.com/ca1105eb-a29a-458d-abbb-34c9b67d7c8a">Status</a> property on the <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> interface.


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

The status information has been skipped. This can occur if a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> is not valid or has not been selected for monitoring.


### -field EnrollDenied

Enrollment has been denied.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/a762d81b-0426-483c-a9c0-70f531f4b6ac">EnrollmentSelectionStatus</a>



<a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a>
 

 

