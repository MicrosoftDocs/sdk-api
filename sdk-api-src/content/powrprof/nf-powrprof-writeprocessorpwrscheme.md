---
UID: NF:powrprof.WriteProcessorPwrScheme
title: WriteProcessorPwrScheme function (powrprof.h)
description: Writes processor power policy settings for the specified power scheme.
helpviewer_keywords: ["WriteProcessorPwrScheme","WriteProcessorPwrScheme function","_win32_writeprocessorpwrscheme","base.writeprocessorpwrscheme","powrprof/WriteProcessorPwrScheme"]
old-location: base\writeprocessorpwrscheme.htm
tech.root: base
ms.assetid: 70e18f50-4774-4a7c-8fe0-7fd6a54aaa90
ms.date: 12/05/2018
ms.keywords: WriteProcessorPwrScheme, WriteProcessorPwrScheme function, _win32_writeprocessorpwrscheme, base.writeprocessorpwrscheme, powrprof/WriteProcessorPwrScheme
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
 - WriteProcessorPwrScheme
 - powrprof/WriteProcessorPwrScheme
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
 - WriteProcessorPwrScheme
---

# WriteProcessorPwrScheme function


## -description

<p class="CCE_Message">[<b>WriteProcessorPwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Writes processor power policy settings for the specified power scheme.

## -parameters

### -param uiID [in]

The index of the power scheme to be written.

### -param pMachineProcessorPowerPolicy [in]

A pointer to a 
<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_processor_power_policy">MACHINE_PROCESSOR_POWER_POLICY</a> structure that contains the power policy settings to be written.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This change does not affect the current system power policy. To apply this change to the current system power policy, call the 
<a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a> function, using the index of this power scheme.

Starting with Windows Vista, power management configuration of the system's processor is controlled through the GUID_PROCESSOR_SETTINGS_SUBGROUP power settings subgroup. Use the <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate individual settings.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_processor_power_policy">MACHINE_PROCESSOR_POWER_POLICY</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-readprocessorpwrscheme">ReadProcessorPwrScheme</a>