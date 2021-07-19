---
UID: NF:powrprof.IsPwrHibernateAllowed
title: IsPwrHibernateAllowed function (powrprof.h)
description: Determines whether the computer supports hibernation.
helpviewer_keywords: ["IsPwrHibernateAllowed","IsPwrHibernateAllowed function","_win32_ispwrhibernateallowed","base.ispwrhibernateallowed","powrprof/IsPwrHibernateAllowed"]
old-location: base\ispwrhibernateallowed.htm
tech.root: base
ms.assetid: fe9d06a8-c021-4cf4-9782-04519f370c5b
ms.date: 12/05/2018
ms.keywords: IsPwrHibernateAllowed, IsPwrHibernateAllowed function, _win32_ispwrhibernateallowed, base.ispwrhibernateallowed, powrprof/IsPwrHibernateAllowed
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
 - IsPwrHibernateAllowed
 - powrprof/IsPwrHibernateAllowed
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
 - IsPwrHibernateAllowed
---

# IsPwrHibernateAllowed function


## -description

<p class="CCE_Message">[<b>IsPwrHibernateAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="/windows/desktop/api/powerbase/nf-powerbase-getpwrcapabilities">GetPwrCapabilities</a> instead.]

Determines whether the computer supports hibernation.



## -returns

If the computer supports hibernation (power state S4) and the file Hiberfil.sys is present on the system, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

## -remarks

This information is also available through the 
<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function. The value is returned in the <b>SystemS4</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>
