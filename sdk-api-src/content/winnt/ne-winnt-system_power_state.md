---
UID: NE:winnt._SYSTEM_POWER_STATE
title: SYSTEM_POWER_STATE (winnt.h)
description: Defines values that are used to specify system power states.
helpviewer_keywords: ["*PSYSTEM_POWER_STATE","PSYSTEM_POWER_STATE","PSYSTEM_POWER_STATE enumeration pointer","PowerSystemHibernate","PowerSystemMaximum","PowerSystemShutdown","PowerSystemSleeping1","PowerSystemSleeping2","PowerSystemSleeping3","PowerSystemUnspecified","PowerSystemWorking","SYSTEM_POWER_STATE","SYSTEM_POWER_STATE enumeration","_win32_system_power_state","base.system_power_state","winnt/PSYSTEM_POWER_STATE","winnt/PowerSystemHibernate","winnt/PowerSystemMaximum","winnt/PowerSystemShutdown","winnt/PowerSystemSleeping1","winnt/PowerSystemSleeping2","winnt/PowerSystemSleeping3","winnt/PowerSystemUnspecified","winnt/PowerSystemWorking","winnt/SYSTEM_POWER_STATE"]
old-location: base\system_power_state.htm
tech.root: base
ms.assetid: 57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE, PSYSTEM_POWER_STATE enumeration pointer, PowerSystemHibernate, PowerSystemMaximum, PowerSystemShutdown, PowerSystemSleeping1, PowerSystemSleeping2, PowerSystemSleeping3, PowerSystemUnspecified, PowerSystemWorking, SYSTEM_POWER_STATE, SYSTEM_POWER_STATE enumeration, _win32_system_power_state, base.system_power_state, winnt/PSYSTEM_POWER_STATE, winnt/PowerSystemHibernate, winnt/PowerSystemMaximum, winnt/PowerSystemShutdown, winnt/PowerSystemSleeping1, winnt/PowerSystemSleeping2, winnt/PowerSystemSleeping3, winnt/PowerSystemUnspecified, winnt/PowerSystemWorking, winnt/SYSTEM_POWER_STATE'
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
targetos: Windows
req.typenames: SYSTEM_POWER_STATE, *PSYSTEM_POWER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_POWER_STATE
 - winnt/_SYSTEM_POWER_STATE
 - PSYSTEM_POWER_STATE
 - winnt/PSYSTEM_POWER_STATE
 - SYSTEM_POWER_STATE
 - winnt/SYSTEM_POWER_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_POWER_STATE
---

# SYSTEM_POWER_STATE enumeration


## -description

Defines values that are used to specify system power states.

## -enum-fields

### -field PowerSystemUnspecified:0

Unspecified system power state.

### -field PowerSystemWorking:1

Specifies system power state S0.

### -field PowerSystemSleeping1:2

Specifies system power state S1.

### -field PowerSystemSleeping2:3

Specifies system power state S2.

### -field PowerSystemSleeping3:4

Specifies system power state S3.

### -field PowerSystemHibernate:5

Specifies system power state S4 (HIBERNATE).

### -field PowerSystemShutdown:6

Specifies system power state S5 (OFF).

### -field PowerSystemMaximum:7

Specifies the maximum enumeration value.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-administrator_power_policy">ADMINISTRATOR_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-global_machine_power_policy">GLOBAL_MACHINE_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a>



<a href="/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a>
