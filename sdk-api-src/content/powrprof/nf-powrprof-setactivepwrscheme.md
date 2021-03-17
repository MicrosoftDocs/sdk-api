---
UID: NF:powrprof.SetActivePwrScheme
title: SetActivePwrScheme function (powrprof.h)
description: Sets the active power scheme.
helpviewer_keywords: ["SetActivePwrScheme","SetActivePwrScheme function","_win32_setactivepwrscheme","base.setactivepwrscheme","powrprof/SetActivePwrScheme"]
old-location: base\setactivepwrscheme.htm
tech.root: base
ms.assetid: f449ff0d-5c22-4c6d-8c88-dc18258a8c6d
ms.date: 12/05/2018
ms.keywords: SetActivePwrScheme, SetActivePwrScheme function, _win32_setactivepwrscheme, base.setactivepwrscheme, powrprof/SetActivePwrScheme
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetActivePwrScheme
 - powrprof/SetActivePwrScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - SetActivePwrScheme
---

# SetActivePwrScheme function


## -description

<p class="CCE_Message">[<b>SetActivePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use 
<a href="/windows/desktop/api/powersetting/nf-powersetting-powersetactivescheme">PowerSetActiveScheme</a> instead.]

Sets the active power scheme.

## -parameters

### -param uiID [in]

The index of the power scheme to be activated.

### -param pGlobalPowerPolicy [in, optional]

A pointer to an optional 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure, which provides global power policy settings to be merged with the power scheme when it becomes active.

### -param pPowerPolicy [in, optional]

A pointer to an optional 
<a href="/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a> structure, which provides power policy settings to be merged with the power scheme when it becomes active.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use this function to make long-term changes to the system configuration. To temporarily keep the system running while an application is performing a task, use the <a href="/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate">SetThreadExecutionState</a> function.

If the power scheme specified by <i>uiID</i> does not exist, the function returns zero.

If <i>lpGlobalPowerPolicy</i> is <b>NULL</b>, the function uses the current global power policy settings set by 
<a href="/windows/desktop/api/powrprof/nf-powrprof-writeglobalpwrpolicy">WriteGlobalPwrPolicy</a>. Otherwise, the settings in the specified structure replace the current global power policy settings.

If <i>lpPowerPolicy</i> is <b>NULL</b>, the function uses the current power policy settings for the power scheme. Otherwise, the settings in the specified structure replace the current power policy settings.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-getactivepwrscheme">GetActivePwrScheme</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/power-schemes">Power Schemes</a>