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

# EnrollmentPolicyServerPropertyFlags enumeration


## -description


The <b>EnrollmentPolicyServerPropertyFlags</b> enumeration specifies the default policy server. It is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method on the <a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a> interface.


## -enum-fields




### -field DefaultNone

No default policy server URL has been specified.


### -field DefaultPolicyServer

The policy server URL returned by <a href="https://msdn.microsoft.com/9d7ba049-4566-423d-b750-ff091dce1e2a">GetPolicyServerUrl</a> is the default value when an URL has not been specified.


## -see-also




<a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

