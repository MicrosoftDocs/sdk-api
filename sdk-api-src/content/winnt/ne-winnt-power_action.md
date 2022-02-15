---
UID: NE:winnt.__unnamed_enum_2
title: POWER_ACTION (winnt.h)
description: Defines values that are used to specify system power action types.
helpviewer_keywords: ["*PPOWER_ACTION","POWER_ACTION","POWER_ACTION enumeration","PPOWER_ACTION","PPOWER_ACTION enumeration pointer","PowerActionHibernate","PowerActionNone","PowerActionReserved","PowerActionShutdown","PowerActionShutdownOff","PowerActionShutdownReset","PowerActionSleep","PowerActionWarmEject","_win32_power_action","base.power_action","winnt/POWER_ACTION","winnt/PPOWER_ACTION","winnt/PowerActionHibernate","winnt/PowerActionNone","winnt/PowerActionReserved","winnt/PowerActionShutdown","winnt/PowerActionShutdownOff","winnt/PowerActionShutdownReset","winnt/PowerActionSleep","winnt/PowerActionWarmEject"]
old-location: base\power_action.htm
tech.root: base
ms.assetid: 815e1f2d-0fc9-446c-ae83-5d5cfea57ab7
ms.date: 12/05/2018
ms.keywords: '*PPOWER_ACTION, POWER_ACTION, POWER_ACTION enumeration, PPOWER_ACTION, PPOWER_ACTION enumeration pointer, PowerActionHibernate, PowerActionNone, PowerActionReserved, PowerActionShutdown, PowerActionShutdownOff, PowerActionShutdownReset, PowerActionSleep, PowerActionWarmEject, _win32_power_action, base.power_action, winnt/POWER_ACTION, winnt/PPOWER_ACTION, winnt/PowerActionHibernate, winnt/PowerActionNone, winnt/PowerActionReserved, winnt/PowerActionShutdown, winnt/PowerActionShutdownOff, winnt/PowerActionShutdownReset, winnt/PowerActionSleep, winnt/PowerActionWarmEject'
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
req.typenames: POWER_ACTION, *PPOWER_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PPOWER_ACTION
 - winnt/PPOWER_ACTION
 - POWER_ACTION
 - winnt/POWER_ACTION
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
 - POWER_ACTION
---

# POWER_ACTION enumeration


## -description

Defines values that are used to specify system power action types.

## -enum-fields

### -field PowerActionNone:0

No system power action.

### -field PowerActionReserved

Reserved; do not use.

### -field PowerActionSleep

Sleep.

### -field PowerActionHibernate

Hibernate.

### -field PowerActionShutdown

Shutdown.

### -field PowerActionShutdownReset

Shutdown and reset.

### -field PowerActionShutdownOff

Shutdown and power off.

### -field PowerActionWarmEject

Warm eject.

### -field PowerActionDisplayOff

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a>



<a href="/windows/desktop/Power/power-management-portal">Power Management</a>



<a href="/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>
