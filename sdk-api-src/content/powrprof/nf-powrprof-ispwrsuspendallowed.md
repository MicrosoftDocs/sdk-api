---
UID: NF:powrprof.IsPwrSuspendAllowed
title: IsPwrSuspendAllowed function (powrprof.h)
description: Determines whether the computer supports the sleep states.
helpviewer_keywords: ["IsPwrSuspendAllowed","IsPwrSuspendAllowed function","_win32_ispwrsuspendallowed","base.ispwrsuspendallowed","powrprof/IsPwrSuspendAllowed"]
old-location: base\ispwrsuspendallowed.htm
tech.root: base
ms.assetid: 66ef2402-b1b8-432e-b47d-240d255fc907
ms.date: 12/05/2018
ms.keywords: IsPwrSuspendAllowed, IsPwrSuspendAllowed function, _win32_ispwrsuspendallowed, base.ispwrsuspendallowed, powrprof/IsPwrSuspendAllowed
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
 - IsPwrSuspendAllowed
 - powrprof/IsPwrSuspendAllowed
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
 - IsPwrSuspendAllowed
---

# IsPwrSuspendAllowed function


## -description

<p class="CCE_Message">[<b>IsPwrSuspendAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="/windows/desktop/api/powerbase/nf-powerbase-getpwrcapabilities">GetPwrCapabilities</a> instead.]

Determines whether the computer supports the sleep states.



## -returns

If the computer supports the sleep states (S1, S2, and S3), the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

## -remarks

This information is also available through the 
<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function. Check the <b>SystemS1</b>, <b>SystemS2</b>, and <b>SystemS3</b> members of the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>
