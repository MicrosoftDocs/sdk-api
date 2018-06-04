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

# EnrollmentEnrollStatus enumeration


## -description



    The <b>EnrollmentEnrollStatus</b> enumeration type specifies the enrollment status of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This enumeration is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property on the <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> interface.


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
 

 

