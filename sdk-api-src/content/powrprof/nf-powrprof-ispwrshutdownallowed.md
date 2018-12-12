---
UID: NF:powrprof.IsPwrShutdownAllowed
title: IsPwrShutdownAllowed function
author: windows-sdk-content
description: Determines whether the computer supports the soft off power state.
old-location: base\ispwrshutdownallowed.htm
tech.root: power
ms.assetid: e48d6f67-225b-40f7-902b-0e65112303b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsPwrShutdownAllowed, IsPwrShutdownAllowed function, _win32_ispwrshutdownallowed, base.ispwrshutdownallowed, powrprof/IsPwrShutdownAllowed
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
 - IsPwrShutdownAllowed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsPwrShutdownAllowed function


## -description


<p class="CCE_Message">[<b>IsPwrShutdownAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Determines whether the computer supports the soft off power state.


## -parameters






## -returns



If the computer supports soft off (power state S5), the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



This information is also available through the 
<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function. The value is returned in the <b>SystemS5</b> member of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa373215(v=VS.85).aspx">SYSTEM_POWER_CAPABILITIES</a> structure.

Starting with Windows Vista, computers must support the soft off power state. Therefore, this function is relevant only to Windows Server 2003 and earlier operating systems.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373215(v=VS.85).aspx">SYSTEM_POWER_CAPABILITIES</a>
 

 

