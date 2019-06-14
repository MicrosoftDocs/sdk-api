---
UID: NE:winnt._SYSTEM_POWER_STATE
title: SYSTEM_POWER_STATE (winnt.h)
author: windows-sdk-content
description: Defines values that are used to specify system power states.
old-location: base\system_power_state.htm
tech.root: power
ms.assetid: 57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE enumeration pointer, PowerSystemHibernate, PowerSystemMaximum, PowerSystemShutdown, PowerSystemSleeping1, PowerSystemSleeping2, PowerSystemSleeping3, PowerSystemUnspecified, PowerSystemWorking, SYSTEM_POWER_STATE, SYSTEM_POWER_STATE enumeration, _win32_system_power_state, base.system_power_state, winnt/PSYSTEM_POWER_STATE, winnt/PowerSystemHibernate, winnt/PowerSystemMaximum, winnt/PowerSystemShutdown, winnt/PowerSystemSleeping1, winnt/PowerSystemSleeping2, winnt/PowerSystemSleeping3, winnt/PowerSystemUnspecified, winnt/PowerSystemWorking, winnt/SYSTEM_POWER_STATE"
ms.topic: enum
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_POWER_STATE
product: Windows
targetos: Windows
req.typenames: SYSTEM_POWER_STATE, *PSYSTEM_POWER_STATE
req.redist: 
ms.custom: 19H1
---

# SYSTEM_POWER_STATE enumeration


## -description


Defines values that are used to specify system power states.


## -enum-fields




### -field PowerSystemUnspecified

Unspecified system power state.


### -field PowerSystemWorking

Specifies system power state S0.


### -field PowerSystemSleeping1

Specifies system power state S1.


### -field PowerSystemSleeping2

Specifies system power state S2.


### -field PowerSystemSleeping3

Specifies system power state S3.


### -field PowerSystemHibernate

Specifies system power state S4 (HIBERNATE).


### -field PowerSystemShutdown

Specifies system power state S5 (OFF).


### -field PowerSystemMaximum

Specifies the maximum enumeration value.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_administrator_power_policy">ADMINISTRATOR_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_global_machine_power_policy">GLOBAL_MACHINE_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_machine_power_policy">MACHINE_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_system_power_policy">SYSTEM_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_user_power_policy">USER_POWER_POLICY</a>
 

 

