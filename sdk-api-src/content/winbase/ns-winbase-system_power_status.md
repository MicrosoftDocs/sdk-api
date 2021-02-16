---
UID: NS:winbase._SYSTEM_POWER_STATUS
title: SYSTEM_POWER_STATUS (winbase.h)
description: Contains information about the power status of the system.
helpviewer_keywords: ["*LPSYSTEM_POWER_STATUS","LPSYSTEM_POWER_STATUS","LPSYSTEM_POWER_STATUS structure pointer","SYSTEM_POWER_STATUS","SYSTEM_POWER_STATUS structure","_SYSTEM_POWER_STATUS","_win32_system_power_status_str","base.system_power_status_str","winbase/LPSYSTEM_POWER_STATUS","winbase/SYSTEM_POWER_STATUS"]
old-location: base\system_power_status_str.htm
tech.root: base
ms.assetid: 4c331239-4222-4650-a0ed-6d605bf376cd
ms.date: 12/05/2018
ms.keywords: '*LPSYSTEM_POWER_STATUS, LPSYSTEM_POWER_STATUS, LPSYSTEM_POWER_STATUS structure pointer, SYSTEM_POWER_STATUS, SYSTEM_POWER_STATUS structure, _SYSTEM_POWER_STATUS, _win32_system_power_status_str, base.system_power_status_str, winbase/LPSYSTEM_POWER_STATUS, winbase/SYSTEM_POWER_STATUS'
req.header: winbase.h
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
req.typenames: SYSTEM_POWER_STATUS, *LPSYSTEM_POWER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_POWER_STATUS
 - winbase/_SYSTEM_POWER_STATUS
 - LPSYSTEM_POWER_STATUS
 - winbase/LPSYSTEM_POWER_STATUS
 - SYSTEM_POWER_STATUS
 - winbase/SYSTEM_POWER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - SYSTEM_POWER_STATUS
---

# SYSTEM_POWER_STATUS structure


## -description

Contains information about the power status of the system.

## -struct-fields

### -field ACLineStatus

The AC power status. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Offline

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Online

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>255</dt>
</dl>
</td>
<td width="60%">
Unknown status

</td>
</tr>
</table>

### -field BatteryFlag

The battery charge status. This member can contain one or more of the following flags. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
High—the battery capacity is at more than 66 percent

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Low—the battery capacity is at less than 33 percent

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Critical—the battery capacity is at less than five percent

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Charging

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>128</dt>
</dl>
</td>
<td width="60%">
No system battery

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>255</dt>
</dl>
</td>
<td width="60%">
Unknown status—unable to read the battery flag information

</td>
</tr>
</table>
 

The value is zero if the battery is not being charged and the battery capacity is between low and high.

### -field BatteryLifePercent

The percentage of full battery charge remaining. This member can be a value in the range 0 to 100, or 255 if status is unknown.

### -field SystemStatusFlag

The status of battery saver. To participate in energy conservation, avoid resource intensive tasks when battery saver is on. To be notified when this value changes, call the <a href="/windows/desktop/api/winuser/nf-winuser-registerpowersettingnotification">RegisterPowerSettingNotification</a> function with the <a href="/windows/desktop/Power/power-setting-guids">power setting GUID</a>, <b>GUID_POWER_SAVING_STATUS</b>. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Battery saver is off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Battery saver on. Save energy where  possible.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This flag and the <b>GUID_POWER_SAVING_STATUS</b> GUID were introduced in Windows 10. This flag was previously reserved, named <b>Reserved1</b>, and had a value of 0.</div>
<div> </div>
For general information about battery saver, see <a href="/windows-hardware/design/component-guidelines/battery-saver">battery saver (in the hardware component guidelines)</a>.

### -field BatteryLifeTime

The number of seconds of battery life remaining, or –1 if remaining seconds are unknown or if the device is connected to AC power.

### -field BatteryFullLifeTime

The number of seconds of battery life when at full charge, or –1 if full battery lifetime is unknown or if the device is connected to AC power.

## -remarks

The system is only capable of estimating <b>BatteryFullLifeTime</b> based on calculations on <b>BatteryLifeTime</b> and <b>BatteryLifePercent</b>. Without smart battery subsystems, this value may not be accurate enough to be useful.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getsystempowerstatus">GetSystemPowerStatus</a>



<a href="/windows/desktop/Power/pbt-apmpowerstatuschange">PBT_APMPOWERSTATUSCHANGE</a>



<a href="/windows-hardware/design/component-guidelines/battery-saver">battery saver (in the hardware component guidelines)</a>