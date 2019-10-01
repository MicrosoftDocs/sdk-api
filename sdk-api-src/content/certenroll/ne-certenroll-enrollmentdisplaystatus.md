---
UID: NE:certenroll.EnrollmentDisplayStatus
title: EnrollmentDisplayStatus (certenroll.h)
author: windows-sdk-content
description: Specifies whether to display enrollment status information in a user interface.
old-location: security\enrollmentdisplaystatus_enum.htm
tech.root: seccertenroll
ms.assetid: bd5019de-1a72-42a6-9ade-74a9252a19eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisplayNo, DisplayYes, EnrollmentDisplayStatus, EnrollmentDisplayStatus enumeration [Security], certenroll/DisplayNo, certenroll/DisplayYes, certenroll/EnrollmentDisplayStatus, security.enrollmentdisplaystatus_enum
ms.topic: enum
f1_keywords: 
 - "certenroll/EnrollmentDisplayStatus"
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
 - EnrollmentDisplayStatus
targetos: Windows
req.typenames: EnrollmentDisplayStatus
req.redist: 
ms.custom: 19H1
---

# EnrollmentDisplayStatus enumeration


## -description


The <b>EnrollmentDisplayStatus</b> enumeration type specifies whether to display enrollment status information in a user interface. This enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> property in the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> interface.


## -enum-fields




### -field DisplayNo

Status is not displayed.


### -field DisplayYes

Status is displayed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
 

 

