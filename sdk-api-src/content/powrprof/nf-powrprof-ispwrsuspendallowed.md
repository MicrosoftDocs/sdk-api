---
UID: NF:powrprof.IsPwrSuspendAllowed
title: IsPwrSuspendAllowed function
author: windows-sdk-content
description: Determines whether the computer supports the sleep states.
old-location: base\ispwrsuspendallowed.htm
tech.root: Power
ms.assetid: 66ef2402-b1b8-432e-b47d-240d255fc907
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IsPwrSuspendAllowed, IsPwrSuspendAllowed function, _win32_ispwrsuspendallowed, base.ispwrsuspendallowed, powrprof/IsPwrSuspendAllowed
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
 - IsPwrSuspendAllowed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsPwrSuspendAllowed function


## -description


<p class="CCE_Message">[<b>IsPwrSuspendAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/bb5cec5f-8d45-4158-824a-023f92af9b69">GetPwrCapabilities</a> instead.]

Determines whether the computer supports the sleep states.


## -parameters






## -returns



If the computer supports the sleep states (S1, S2, and S3), the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



This information is also available through the 
<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function. Check the <b>SystemS1</b>, <b>SystemS2</b>, and <b>SystemS3</b> members of the 
<a href="https://msdn.microsoft.com/aa0af56e-59b3-4d0d-b356-a4046d8754ef">SYSTEM_POWER_CAPABILITIES</a> structure.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/aa0af56e-59b3-4d0d-b356-a4046d8754ef">SYSTEM_POWER_CAPABILITIES</a>
 

 

