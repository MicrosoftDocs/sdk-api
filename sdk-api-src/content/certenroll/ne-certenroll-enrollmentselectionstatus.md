---
UID: NE:certenroll.EnrollmentSelectionStatus
title: EnrollmentSelectionStatus
author: windows-sdk-content
description: Specifies whether the enrollment status of an object will be monitored during the enrollment process.
old-location: security\enrollmentselectionstatus_enum.htm
tech.root: seccertenroll
ms.assetid: a762d81b-0426-483c-a9c0-70f531f4b6ac
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: EnrollmentSelectionStatus, EnrollmentSelectionStatus enumeration [Security], SelectedNo, SelectedYes, certenroll/EnrollmentSelectionStatus, certenroll/SelectedNo, certenroll/SelectedYes, security.enrollmentselectionstatus_enum
ms.prod: windows
ms.technology: windows-sdk
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


The <b>EnrollmentSelectionStatus</b> enumeration type specifies whether the enrollment status of an object will be monitored during the enrollment process. Cryptographic providers, individual enrollment objects in a collection, and <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authorities</a> are often monitored and their status displayed in a user interface. A value of this enumeration can be specified or retrieved by using the <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> interface. An <b>IX509EnrollmentStatus</b> object can be retrieved from the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> objects.


## -enum-fields




### -field SelectedNo

The enrollment status is not monitored.


### -field SelectedYes

The enrollment status is monitored.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a>
 

 

