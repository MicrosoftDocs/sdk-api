---
UID: NF:powrprof.SetSuspendState
title: SetSuspendState function
author: windows-sdk-content
description: Suspends the system by shutting power down. Depending on the Hibernate parameter, the system either enters a suspend (sleep) state or hibernation (S4).
old-location: base\setsuspendstate.htm
tech.root: power
ms.assetid: 63cb6574-8c0d-4bcb-832c-7088447a5c04
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SetSuspendState, SetSuspendState function, _win32_setsuspendstate, base.setsuspendstate, powrprof/SetSuspendState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetSuspendState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetSuspendState
: 
---

# SetSuspendState function


## -description


Suspends the system by shutting power down. Depending on the <i>Hibernate</i> 
    parameter, the system either enters a suspend (sleep) state or hibernation (S4).


## -parameters




### -param bHibernate [in]

If this parameter is <b>TRUE</b>, the system hibernates. If the parameter is 
      <b>FALSE</b>, the system is suspended.


### -param bForce [in]

This parameter has no effect.
      


### -param bWakeupEventsDisabled [in]

If this parameter is <b>TRUE</b>, the system disables all wake events. If the parameter 
      is <b>FALSE</b>, any system wake events remain enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. To enable the 
    <b>SE_SHUTDOWN_NAME</b> privilege, use the 
    <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function. For more 
    information, see <a href="https://msdn.microsoft.com/b8e47d04-07c1-4d57-8209-6b0c397476e5">Changing Privileges in a 
    Token</a>.

An application may use <b>SetSuspendState</b> to 
    transition the system from the working state to the standby (sleep), or optionally, hibernate (S4) state. This 
    function is similar to the <a href="https://msdn.microsoft.com/58cf4e29-2a2e-499a-85ce-0034f4323cfe">SetSystemPowerState</a> 
    function.

For more information on using PowrProf.h, see 
    <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>. For information about events that can wake the system, see <a href="https://msdn.microsoft.com/b7326b09-0829-4e76-80d0-e4ecdf7f556e">System Wake-up Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/83cb0fdc-437e-4d03-87f0-6a416281c0d5">PBT_APMQUERYSUSPEND</a>



<a href="https://msdn.microsoft.com/61b177a0-4cff-4740-bed8-a46c06c43be8">PBT_APMSUSPEND</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

