---
UID: NE:certenroll.EnrollmentSelectionStatus
title: EnrollmentSelectionStatus
author: windows-sdk-content
description: Specifies whether the enrollment status of an object will be monitored during the enrollment process.
old-location: security\enrollmentselectionstatus_enum.htm
tech.root: SecCertEnroll
ms.assetid: a762d81b-0426-483c-a9c0-70f531f4b6ac
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnrollmentSelectionStatus, EnrollmentSelectionStatus enumeration [Security], SelectedNo, SelectedYes, certenroll/EnrollmentSelectionStatus, certenroll/SelectedNo, certenroll/SelectedYes, security.enrollmentselectionstatus_enum
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
 - EnrollmentSelectionStatus
product: Windows
targetos: Windows
req.typenames: EnrollmentSelectionStatus
req.redist: 
---

# EnrollmentSelectionStatus enumeration


## -description


The <b>EnrollmentSelectionStatus</b> enumeration type specifies whether the enrollment status of an object will be monitored during the enrollment process. Cryptographic providers, individual enrollment objects in a collection, and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> are often monitored and their status displayed in a user interface. A value of this enumeration can be specified or retrieved by using the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property on the <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> interface. An <b>IX509EnrollmentStatus</b> object can be retrieved from the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> and <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects.


## -enum-fields




### -field SelectedNo

The enrollment status is not monitored.


### -field SelectedYes

The enrollment status is monitored.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a>
 

 

