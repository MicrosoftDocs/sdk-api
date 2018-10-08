---
UID: NE:winnt._SYSTEM_POWER_STATE
title: "_SYSTEM_POWER_STATE"
author: windows-sdk-content
description: Defines values that are used to specify system power states.
old-location: base\system_power_state.htm
tech.root: power
ms.assetid: 57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE enumeration pointer, PowerSystemHibernate, PowerSystemMaximum, PowerSystemShutdown, PowerSystemSleeping1, PowerSystemSleeping2, PowerSystemSleeping3, PowerSystemUnspecified, PowerSystemWorking, SYSTEM_POWER_STATE, SYSTEM_POWER_STATE enumeration, _SYSTEM_POWER_STATE, _win32_system_power_state, base.system_power_state, winnt/PSYSTEM_POWER_STATE, winnt/PowerSystemHibernate, winnt/PowerSystemMaximum, winnt/PowerSystemShutdown, winnt/PowerSystemSleeping1, winnt/PowerSystemSleeping2, winnt/PowerSystemSleeping3, winnt/PowerSystemUnspecified, winnt/PowerSystemWorking, winnt/SYSTEM_POWER_STATE"
ms.prod: windows
ms.technology: windows-sdk
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
---

# _SYSTEM_POWER_STATE enumeration


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




<a href="https://msdn.microsoft.com/abd2e2c5-1056-4985-ae07-a40d53bb17b1">ADMINISTRATOR_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/79b57da4-0125-427b-aec7-7ca4c9bfb870">GLOBAL_MACHINE_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/41dca573-a73d-430c-9bd3-083e72aecbdc">MACHINE_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/f78cd97f-586f-4091-ab4a-5f109a0f679a">Power Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/aa0af56e-59b3-4d0d-b356-a4046d8754ef">SYSTEM_POWER_CAPABILITIES</a>



<a href="https://msdn.microsoft.com/0e73e94d-e529-46fb-b3e5-a79ba2c05713">SYSTEM_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/616c45f6-ec80-42d9-a485-e9e778f2b971">USER_POWER_POLICY</a>
 

 

