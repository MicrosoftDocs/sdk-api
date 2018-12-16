---
UID: NF:powerbase.GetPwrCapabilities
title: GetPwrCapabilities function
author: windows-sdk-content
description: Retrieves information about the system power capabilities.
old-location: base\getpwrcapabilities.htm
tech.root: power
ms.assetid: bb5cec5f-8d45-4158-824a-023f92af9b69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPwrCapabilities, GetPwrCapabilities function, _win32_getpwrcapabilities, base.getpwrcapabilities, powerbase/GetPwrCapabilities, powrprof/GetPwrCapabilities
ms.topic: function
req.header: powerbase.h
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
 - API-MS-Win-power-base-l1-1-0.dll
api_name:
 - GetPwrCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPwrCapabilities function


## -description


Retrieves information about the system power capabilities.


## -parameters




### -param lpspc [out]

A pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Aa373215(v=VS.85).aspx">SYSTEM_POWER_CAPABILITIES</a> structure that receives the information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function retrieves detailed information about the current system power management hardware resources and capabilities. This includes information about the presence of hardware features such as power buttons, lid switches, and batteries. Other details returned include information about current power management capabilities and configurations that can change dynamically, such as the minimum sleep state currently supported, which may change as new drivers are introduced into the system, or the presence of the system hibernation file.

This information is also available through the 
<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function, using the SystemPowerCapabilities level.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373215(v=VS.85).aspx">SYSTEM_POWER_CAPABILITIES</a>
 

 

