---
UID: NF:powrprof.ReadGlobalPwrPolicy
title: ReadGlobalPwrPolicy function (powrprof.h)
description: Retrieves the current global power policy settings.
helpviewer_keywords: ["ReadGlobalPwrPolicy","ReadGlobalPwrPolicy function","_win32_readglobalpwrpolicy","base.readglobalpwrpolicy","powrprof/ReadGlobalPwrPolicy"]
old-location: base\readglobalpwrpolicy.htm
tech.root: base
ms.assetid: 65da3d9f-b688-4d41-9da0-05159297d169
ms.date: 12/05/2018
ms.keywords: ReadGlobalPwrPolicy, ReadGlobalPwrPolicy function, _win32_readglobalpwrpolicy, base.readglobalpwrpolicy, powrprof/ReadGlobalPwrPolicy
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
 - ReadGlobalPwrPolicy
 - powrprof/ReadGlobalPwrPolicy
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
 - ReadGlobalPwrPolicy
---

# ReadGlobalPwrPolicy function


## -description

<p class="CCE_Message">[<b>ReadGlobalPwrPolicy</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the current global power policy settings.

## -parameters

### -param pGlobalPowerPolicy [out]

A pointer to a 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure that receives the information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure contains policy settings that are common to all power schemes. This structure contains both user and computer policy settings.

Starting with Windows Vista, use the <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> function to enumerate power settings for a specified scheme and the power read functions to retrieve individual settings. 

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-writeglobalpwrpolicy">WriteGlobalPwrPolicy</a>