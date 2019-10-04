---
UID: NF:powrprof.IsPwrHibernateAllowed
title: IsPwrHibernateAllowed function (powrprof.h)
author: windows-sdk-content
description: Determines whether the computer supports hibernation.
old-location: base\ispwrhibernateallowed.htm
tech.root: power
ms.assetid: fe9d06a8-c021-4cf4-9782-04519f370c5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsPwrHibernateAllowed, IsPwrHibernateAllowed function, _win32_ispwrhibernateallowed, base.ispwrhibernateallowed, powrprof/IsPwrHibernateAllowed
ms.topic: function
f1_keywords: 
 - "powrprof/IsPwrHibernateAllowed"
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
 - IsPwrHibernateAllowed
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsPwrHibernateAllowed function


## -description


<p class="CCE_Message">[<b>IsPwrHibernateAllowed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-getpwrcapabilities">GetPwrCapabilities</a> instead.]

Determines whether the computer supports hibernation.


## -parameters






## -returns



If the computer supports hibernation (power state S4) and the file Hiberfil.sys is present on the system, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



This information is also available through the 
<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a> function. The value is returned in the <b>SystemS4</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure.

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>
 

 

