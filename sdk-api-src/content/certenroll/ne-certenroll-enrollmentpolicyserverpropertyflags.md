---
UID: NE:certenroll.EnrollmentPolicyServerPropertyFlags
title: EnrollmentPolicyServerPropertyFlags
author: windows-sdk-content
description: Specifies the default policy server.
old-location: security\enrollmentpolicyserverpropertyflags.htm
tech.root: seccertenroll
ms.assetid: 531502ac-8e89-46ee-a426-86e22a9dbe8d
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: DefaultNone, DefaultPolicyServer, EnrollmentPolicyServerPropertyFlags, EnrollmentPolicyServerPropertyFlags enumeration [Security], certenroll/DefaultNone, certenroll/DefaultPolicyServer, certenroll/EnrollmentPolicyServerPropertyFlags, security.enrollmentpolicyserverpropertyflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: EnrollmentPolicyServerPropertyFlags
req.redist: 
---

# EnrollmentPolicyServerPropertyFlags enumeration


## -description


The <b>EnrollmentPolicyServerPropertyFlags</b> enumeration specifies the default policy server. It is used by the <a href="https://msdn.microsoft.com/en-us/library/Ee351591(v=VS.85).aspx">Initialize</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Ee338624(v=VS.85).aspx">ICertPropertyEnrollmentPolicyServer</a> interface.


## -enum-fields




### -field DefaultNone

No default policy server URL has been specified.


### -field DefaultPolicyServer

The policy server URL returned by <a href="https://msdn.microsoft.com/en-us/library/Ee338635(v=VS.85).aspx">GetPolicyServerUrl</a> is the default value when an URL has not been specified.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee338624(v=VS.85).aspx">ICertPropertyEnrollmentPolicyServer</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee351591(v=VS.85).aspx">Initialize</a>
 

 

