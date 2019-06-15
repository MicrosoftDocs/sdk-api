---
UID: NF:powrprof.ReadProcessorPwrScheme
title: ReadProcessorPwrScheme function (powrprof.h)
author: windows-sdk-content
description: Retrieves the processor power policy settings for the specified power scheme.
old-location: base\readprocessorpwrscheme.htm
tech.root: power
ms.assetid: 740095a7-9def-48a3-9cbb-1da91b052321
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReadProcessorPwrScheme, ReadProcessorPwrScheme function, _win32_readprocessorpwrscheme, base.readprocessorpwrscheme, powrprof/ReadProcessorPwrScheme
ms.topic: function
f1_keywords: ["powrprof/ReadProcessorPwrScheme"]
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
 - ReadProcessorPwrScheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReadProcessorPwrScheme function


## -description


<p class="CCE_Message">[<b>ReadProcessorPwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the processor power policy settings for the specified power scheme.


## -parameters




### -param uiID [in]

The index of the power scheme to be read.


### -param pMachineProcessorPowerPolicy [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_machine_processor_power_policy">MACHINE_PROCESSOR_POWER_POLICY</a> structure that receives the processor power policy settings.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_machine_processor_power_policy">MACHINE_PROCESSOR_POWER_POLICY</a> structure contains processor power policy settings for use while the system is running on AC power or battery power.

Starting with Windows Vista, power management configuration of the system's processor is controlled through the GUID_PROCESSOR_SETTINGS_SUBGROUP power settings subgroup. Use the <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate individual settings.

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_machine_processor_power_policy">MACHINE_PROCESSOR_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writeprocessorpwrscheme">WriteProcessorPwrScheme</a>
 

 

