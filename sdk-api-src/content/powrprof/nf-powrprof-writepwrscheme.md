---
UID: NF:powrprof.WritePwrScheme
title: WritePwrScheme function (powrprof.h)
description: Writes policy settings that are unique to the specified power scheme.
helpviewer_keywords: ["WritePwrScheme","WritePwrScheme function","_win32_writepwrscheme","base.writepwrscheme","powrprof/WritePwrScheme"]
old-location: base\writepwrscheme.htm
tech.root: base
ms.assetid: b9233601-6848-41c4-bb58-27decad60ba5
ms.date: 12/05/2018
ms.keywords: WritePwrScheme, WritePwrScheme function, _win32_writepwrscheme, base.writepwrscheme, powrprof/WritePwrScheme
f1_keywords:
- powrprof/WritePwrScheme
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
- WritePwrScheme
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WritePwrScheme function


## -description


<p class="CCE_Message">[<b>WritePwrScheme</b> is no longer available for use as of Windows Vista. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate power settings for a specified scheme, and the power write functions to write individual settings.]

Writes policy settings that are unique to the specified power scheme.


## -parameters




### -param puiID [in]

The index of the power scheme to be written. If a power scheme with the same index already exists, it is replaced. Otherwise, a new power scheme is created.


### -param lpszSchemeName [in]

The name of the power scheme.


### -param lpszDescription [in, optional]

The description of the power scheme.


### -param lpScheme [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a> structure that contains the power policy settings to be written.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This change does not affect the current system power policy. To apply this change to the current system power policy, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a> function with the index of this power scheme.

Power policy schemes written using 
<b>WritePwrScheme</b> are permanently stored in the system registry hives, and remain available for use in the Power Options control panel program, or by subsequent calls to the power scheme API. To permanently remove a power scheme from the system, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-deletepwrscheme">DeletePwrScheme</a> function.

For more information about using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-deletepwrscheme">DeletePwrScheme</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-readpwrscheme">ReadPwrScheme</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>
 

 

