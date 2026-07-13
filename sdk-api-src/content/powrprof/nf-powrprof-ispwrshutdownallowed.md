---
UID: NF:powrprof.IsPwrShutdownAllowed
title: IsPwrShutdownAllowed function (powrprof.h)
description: Determines whether the computer supports the soft off power state.
helpviewer_keywords: ["IsPwrShutdownAllowed","IsPwrShutdownAllowed function","_win32_ispwrshutdownallowed","base.ispwrshutdownallowed","powrprof/IsPwrShutdownAllowed"]
old-location: base\ispwrshutdownallowed.htm
tech.root: base
ms.assetid: e48d6f67-225b-40f7-902b-0e65112303b9
ms.date: 12/05/2018
ms.keywords: IsPwrShutdownAllowed, IsPwrShutdownAllowed function, _win32_ispwrshutdownallowed, base.ispwrshutdownallowed, powrprof/IsPwrShutdownAllowed
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
 - IsPwrShutdownAllowed
 - powrprof/IsPwrShutdownAllowed
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
 - IsPwrShutdownAllowed
---

# IsPwrShutdownAllowed function


## -description

<p class="CCE_Message">[<b>IsPwrShutdownAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Determines whether the computer supports the soft off power state.



## -returns

If the computer supports soft off (power state S5), the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

## -remarks

This information is also available through the 
<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function. The value is returned in the <b>SystemS5</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure.

Starting with Windows Vista, computers must support the soft off power state. Therefore, this function is relevant only to Windows Server 2003 and earlier operating systems.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>
