---
UID: NF:powrprof.IsPwrHibernateAllowed
title: IsPwrHibernateAllowed function
author: windows-sdk-content
description: Determines whether the computer supports hibernation.
old-location: base\ispwrhibernateallowed.htm
tech.root: Power
ms.assetid: fe9d06a8-c021-4cf4-9782-04519f370c5b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IsPwrHibernateAllowed, IsPwrHibernateAllowed function, _win32_ispwrhibernateallowed, base.ispwrhibernateallowed, powrprof/IsPwrHibernateAllowed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - IsPwrHibernateAllowed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsPwrHibernateAllowed function


## -description


<p class="CCE_Message">[<b>IsPwrHibernateAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/bb5cec5f-8d45-4158-824a-023f92af9b69">GetPwrCapabilities</a> instead.]

Determines whether the computer supports hibernation.


## -parameters






## -returns



If the computer supports hibernation (power state S4) and the file Hiberfil.sys is present on the system, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



This information is also available through the 
<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function. The value is returned in the <b>SystemS4</b> member of the 
<a href="https://msdn.microsoft.com/aa0af56e-59b3-4d0d-b356-a4046d8754ef">SYSTEM_POWER_CAPABILITIES</a> structure.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/aa0af56e-59b3-4d0d-b356-a4046d8754ef">SYSTEM_POWER_CAPABILITIES</a>
 

 

