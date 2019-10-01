---
UID: NF:powrprof.WriteGlobalPwrPolicy
title: WriteGlobalPwrPolicy function (powrprof.h)
author: windows-sdk-content
description: Writes global power policy settings.
old-location: base\writeglobalpwrpolicy.htm
tech.root: power
ms.assetid: 293dc3a5-5e6b-4709-8439-67d2339740e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WriteGlobalPwrPolicy, WriteGlobalPwrPolicy function, _win32_writeglobalpwrpolicy, base.writeglobalpwrpolicy, powrprof/WriteGlobalPwrPolicy
ms.topic: function
f1_keywords:
- powrprof/WriteGlobalPwrPolicy
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
- WriteGlobalPwrPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WriteGlobalPwrPolicy function


## -description


<p class="CCE_Message">[<b>WriteGlobalPwrPolicy</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Writes global power policy settings.


## -parameters




### -param pGlobalPowerPolicy [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure that contains the power policy settings to be written.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The function replaces any existing global power policy settings. Each user has a separate global power scheme, which contains power policy settings that apply to all power schemes for that user.

Starting with Windows Vista, use the <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate power settings for a specified scheme and the power write functions to write individual settings. 

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-readglobalpwrpolicy">ReadGlobalPwrPolicy</a>
 

 

