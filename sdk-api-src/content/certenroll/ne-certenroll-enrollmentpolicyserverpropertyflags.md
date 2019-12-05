---
UID: NE:certenroll.EnrollmentPolicyServerPropertyFlags
title: EnrollmentPolicyServerPropertyFlags (certenroll.h)
description: Specifies the default policy server.
old-location: security\enrollmentpolicyserverpropertyflags.htm
tech.root: seccertenroll
ms.assetid: 531502ac-8e89-46ee-a426-86e22a9dbe8d
ms.date: 12/05/2018
ms.keywords: DefaultNone, DefaultPolicyServer, EnrollmentPolicyServerPropertyFlags, EnrollmentPolicyServerPropertyFlags enumeration [Security], certenroll/DefaultNone, certenroll/DefaultPolicyServer, certenroll/EnrollmentPolicyServerPropertyFlags, security.enrollmentpolicyserverpropertyflags
ms.topic: enum
f1_keywords:
- certenroll/EnrollmentPolicyServerPropertyFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Certenroll.h
api_name:
- EnrollmentPolicyServerPropertyFlags
targetos: Windows
req.typenames: EnrollmentPolicyServerPropertyFlags
req.redist: 
ms.custom: 19H1
---

# EnrollmentPolicyServerPropertyFlags enumeration


## -description


The <b>EnrollmentPolicyServerPropertyFlags</b> enumeration specifies the default policy server. It is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> interface.


## -enum-fields




### -field DefaultNone

No default policy server URL has been specified.


### -field DefaultPolicyServer

The policy server URL returned by <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-getpolicyserverurl">GetPolicyServerUrl</a> is the default value when an URL has not been specified.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a>
 

 

