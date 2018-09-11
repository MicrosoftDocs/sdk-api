---
UID: NF:certenroll.IX509Enrollment.get_EnrollmentContext
title: IX509Enrollment::get_EnrollmentContext
author: windows-sdk-content
description: Retrieves an enrollment context that identifies whether the certificate is intended for a computer or an end-user.
old-location: security\ix509enrollment_enrollmentcontext_property.htm
tech.root: SecCertEnroll
ms.assetid: 48bfe2cd-1d17-42a9-8068-b635fd220911
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnrollmentContext property [Security], EnrollmentContext property [Security],IX509Enrollment interface, IX509Enrollment interface [Security],EnrollmentContext property, IX509Enrollment.EnrollmentContext, IX509Enrollment.get_EnrollmentContext, IX509Enrollment::EnrollmentContext, IX509Enrollment::get_EnrollmentContext, certenroll/IX509Enrollment::EnrollmentContext, certenroll/IX509Enrollment::get_EnrollmentContext, get_EnrollmentContext, security.ix509enrollment_enrollmentcontext_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.EnrollmentContext
 - IX509Enrollment.get_EnrollmentContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment::get_EnrollmentContext


## -description


The <b>EnrollmentContext</b> property retrieves an enrollment context that identifies whether the certificate is intended for a computer or an end-user.

This property is read-only.


## -parameters


## -remarks



Before calling this property, you must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378046(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377872(v=VS.85).aspx">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378023(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

