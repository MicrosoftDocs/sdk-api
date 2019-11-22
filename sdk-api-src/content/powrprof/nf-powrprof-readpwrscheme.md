---
UID: NF:powrprof.ReadPwrScheme
title: ReadPwrScheme function (powrprof.h)

description: Retrieves the power policy settings that are unique to the specified power scheme.
old-location: base\readpwrscheme.htm
tech.root: power
ms.assetid: a8d93820-b652-4358-8039-8987fac95dca

ms.date: 12/05/2018
ms.keywords: ReadPwrScheme, ReadPwrScheme function, _win32_readpwrscheme, base.readpwrscheme, powrprof/ReadPwrScheme
ms.topic: function
f1_keywords:
- powrprof/ReadPwrScheme
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
- ReadPwrScheme
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReadPwrScheme function


## -description


<p class="CCE_Message">[<b>ReadPwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the power policy settings that are unique to the specified power scheme.


## -parameters




### -param uiID [in]

The index of the power scheme to be read.


### -param pPowerPolicy [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a> structure that receives the power policy settings.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If the power scheme specified does not exist, the function returns <b>FALSE</b>.

To retrieve information about the power policy settings currently in use by the system, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-getactivepwrscheme">GetActivePwrScheme</a> function. To retrieve additional information about the current power policy settings, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function.

Starting with Windows Vista, use the <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate power settings for a specified scheme and the power read functions to retrieve individual settings. 

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-getactivepwrscheme">GetActivePwrScheme</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>
 

 

