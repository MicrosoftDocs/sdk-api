---
UID: NF:powrprof.GetCurrentPowerPolicies
title: GetCurrentPowerPolicies function (powrprof.h)
description: Retrieves the current system power policy settings.
helpviewer_keywords: ["GetCurrentPowerPolicies","GetCurrentPowerPolicies function","_win32_getcurrentpowerpolicies","base.getcurrentpowerpolicies","powrprof/GetCurrentPowerPolicies"]
old-location: base\getcurrentpowerpolicies.htm
tech.root: base
ms.assetid: 9a834fb6-35ae-4d36-885c-0d81cd39e9a6
ms.date: 12/05/2018
ms.keywords: GetCurrentPowerPolicies, GetCurrentPowerPolicies function, _win32_getcurrentpowerpolicies, base.getcurrentpowerpolicies, powrprof/GetCurrentPowerPolicies
f1_keywords:
- powrprof/GetCurrentPowerPolicies
dev_langs:
- c++
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
- GetCurrentPowerPolicies
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentPowerPolicies function


## -description


Retrieves the current system power policy settings.


## -parameters




### -param pGlobalPowerPolicy [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure that receives the current global power policy settings.


### -param pPowerPolicy [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a> structure that receives the power policy settings that are unique to the active power scheme.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To update the current power policy settings, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writeglobalpwrpolicy">WriteGlobalPwrPolicy</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a> functions.

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writeglobalpwrpolicy">WriteGlobalPwrPolicy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>
 

 

