---
UID: NF:powerbase.GetPwrCapabilities
title: GetPwrCapabilities function (powerbase.h)
description: Retrieves information about the system power capabilities.helpviewer_keywords: ["GetPwrCapabilities","GetPwrCapabilities function","_win32_getpwrcapabilities","base.getpwrcapabilities","powerbase/GetPwrCapabilities","powrprof/GetPwrCapabilities"]
old-location: base\getpwrcapabilities.htm
tech.root: power
ms.assetid: bb5cec5f-8d45-4158-824a-023f92af9b69
ms.date: 12/05/2018
ms.keywords: GetPwrCapabilities, GetPwrCapabilities function, _win32_getpwrcapabilities, base.getpwrcapabilities, powerbase/GetPwrCapabilities, powrprof/GetPwrCapabilities
f1_keywords:
- powerbase/GetPwrCapabilities
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetPwrCapabilities function


## -description


Retrieves information about the system power capabilities.


## -parameters




### -param lpspc [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure that receives the information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function retrieves detailed information about the current system power management hardware resources and capabilities. This includes information about the presence of hardware features such as power buttons, lid switches, and batteries. Other details returned include information about current power management capabilities and configurations that can change dynamically, such as the minimum sleep state currently supported, which may change as new drivers are introduced into the system, or the presence of the system hibernation file.

This information is also available through the 
<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function, using the SystemPowerCapabilities level.

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>
 

 

