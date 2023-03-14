---
UID: NS:winnt.SYSTEM_POWER_CAPABILITIES
title: SYSTEM_POWER_CAPABILITIES (winnt.h)
description: Contains information about the power capabilities of the system.
helpviewer_keywords: ["*PSYSTEM_POWER_CAPABILITIES","PSYSTEM_POWER_CAPABILITIES","PSYSTEM_POWER_CAPABILITIES structure pointer","SYSTEM_POWER_CAPABILITIES","SYSTEM_POWER_CAPABILITIES structure","_win32_system_power_capabilities_str","base.system_power_capabilities_str","winnt/PSYSTEM_POWER_CAPABILITIES","winnt/SYSTEM_POWER_CAPABILITIES"]
old-location: base\system_power_capabilities_str.htm
tech.root: base
ms.assetid: aa0af56e-59b3-4d0d-b356-a4046d8754ef
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_POWER_CAPABILITIES, PSYSTEM_POWER_CAPABILITIES, PSYSTEM_POWER_CAPABILITIES structure pointer, SYSTEM_POWER_CAPABILITIES, SYSTEM_POWER_CAPABILITIES structure, _win32_system_power_capabilities_str, base.system_power_capabilities_str, winnt/PSYSTEM_POWER_CAPABILITIES, winnt/SYSTEM_POWER_CAPABILITIES'
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
req.typenames: SYSTEM_POWER_CAPABILITIES, *PSYSTEM_POWER_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSYSTEM_POWER_CAPABILITIES
 - winnt/PSYSTEM_POWER_CAPABILITIES
 - SYSTEM_POWER_CAPABILITIES
 - winnt/SYSTEM_POWER_CAPABILITIES
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
 - SYSTEM_POWER_CAPABILITIES
---

# SYSTEM_POWER_CAPABILITIES structure


## -description

Contains information about the power capabilities of the system.

## -struct-fields

### -field PowerButtonPresent

If this member is <b>TRUE</b>, there is a system power button.

### -field SleepButtonPresent

If this member is <b>TRUE</b>, there is a system sleep button.

### -field LidPresent

If this member is <b>TRUE</b>, there is a lid switch.

### -field SystemS1

If this member is <b>TRUE</b>, the operating system supports <a href="/windows/desktop/Power/system-power-states">sleep state S1</a>.

### -field SystemS2

If this member is <b>TRUE</b>, the operating system supports <a href="/windows/desktop/Power/system-power-states">sleep state S2</a>.

### -field SystemS3

If this member is <b>TRUE</b>, the operating system supports <a href="/windows/desktop/Power/system-power-states">sleep state S3</a>.

### -field SystemS4

If this member is <b>TRUE</b>, the operating system supports <a href="/windows/desktop/Power/system-power-states">sleep state S4</a> (hibernation).

### -field SystemS5

If this member is <b>TRUE</b>, the operating system supports <a href="/windows/desktop/Power/system-power-states">power off state S5</a> (soft off).

### -field HiberFilePresent

If this member is <b>TRUE</b>, the system hibernation file is present.

### -field FullWake

If this member is <b>TRUE</b>, the system supports wake capabilities.

### -field VideoDimPresent

If this member is <b>TRUE</b>, the system supports video display dimming 
      capabilities.

### -field ApmPresent

If this member is <b>TRUE</b>, the system supports APM BIOS power management 
      features.

### -field UpsPresent

If this member is <b>TRUE</b>, there is an uninterruptible power supply 
      (UPS).

### -field ThermalControl

If this member is <b>TRUE</b>, the system supports thermal zones.

### -field ProcessorThrottle

If this member is <b>TRUE</b>, the system supports processor throttling.

### -field ProcessorMinThrottle

The minimum level of system processor throttling supported, expressed as a percentage.

### -field ProcessorThrottleScale

### -field spare2

### -field ProcessorMaxThrottle

The maximum level of system processor throttling supported, expressed as a percentage.

### -field FastSystemS4

If this member is <b>TRUE</b>, the system supports the <a href="/windows/desktop/Power/system-power-states">hybrid sleep state</a>.

### -field Hiberboot

### -field WakeAlarmPresent

If this member is <b>TRUE</b>, the platform has support for ACPI wake alarm devices.  For more details on wake alarm devices, please see the ACPI specification section 9.18.

### -field AoAc

If this member is <b>TRUE</b>, the system supports the S0 low power idle model.

### -field DiskSpinDown

If this member is <b>TRUE</b>, the system supports allowing the removal of power to 
      fixed disk devices.

### -field HiberFileType

### -field AoAcConnectivitySupported

### -field spare3

Reserved.

### -field SystemBatteriesPresent

If this member is <b>TRUE</b>, there are one or more batteries in the system.

### -field BatteriesAreShortTerm

If this member is <b>TRUE</b>, the system batteries are short-term. Short-term batteries 
      are used in uninterruptible power supplies (UPS).

### -field BatteryScale

A <a href="/windows/desktop/api/winnt/ns-winnt-battery_reporting_scale">BATTERY_REPORTING_SCALE</a> structure 
      that contains information about how system battery metrics are reported.

### -field AcOnLineWake

The lowest <a href="/windows/desktop/Power/system-power-states">system sleep state</a> (Sx) that will generate a wake event when the system is on AC power. This 
      member must be one of the <a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> 
      enumeration type values.

### -field SoftLidWake

The lowest <a href="/windows/desktop/Power/system-power-states">system sleep state</a> (Sx) that will generate a wake event via the lid switch. This member must be 
      one of the <a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration 
      type values.

### -field RtcWake

The lowest <a href="/windows/desktop/Power/system-power-states">system sleep state</a> (Sx) supported by hardware that will generate a wake event via the Real Time Clock (RTC). This 
      member must be one of the 
      <a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type 
      values. 

To wake the computer using the RTC, the operating system must also support waking from the sleep state the computer is in when the RTC generates the wake event. Therefore, the  effective lowest sleep state from which an RTC wake event can wake the computer is the lowest sleep state supported by the operating system that is  equal to or higher than  the  value  of <b>RtcWake</b>.  To determine  the sleep states that the operating system supports, check the   <b>SystemS1</b>, <b>SystemS2</b>, <b>SystemS3</b>, and <b>SystemS4</b> members.

### -field MinDeviceWakeState

The minimum allowable <a href="/windows/desktop/Power/system-power-states">system power state</a> supporting wake events. This member must be one of the 
      <a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type 
      values. Note that this state may change as different device drivers are installed on the system.

### -field DefaultLowLatencyWake

The default <a href="/windows/desktop/Power/system-power-states">system power state</a> used if an application calls 
      <a href="/windows/desktop/api/winbase/nf-winbase-requestwakeuplatency">RequestWakeupLatency</a> with 
      <b>LT_LOWEST_LATENCY</b>. This member must be one of the 
      <a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type 
      values.

### -field HiberBoot

If this member is set to <b>TRUE</b>, the system is currently capable of performing a fast startup transition.  This setting is based on whether the machine is capable of hibernate, whether the machine currently has hibernate enabled (hiberfile exists), and the local and group policy settings for using hibernate (including the Hibernate option in the Power control panel).

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/Power/system-power-states">System Power States</a>

