---
UID: NS:winnt.POWER_ACTION_POLICY
title: POWER_ACTION_POLICY (winnt.h)
description: Contains information used to set the system power state.
helpviewer_keywords: ["*PPOWER_ACTION_POLICY","POWER_ACTION_CRITICAL","POWER_ACTION_DISABLE_WAKES","POWER_ACTION_LIGHTEST_FIRST","POWER_ACTION_LOCK_CONSOLE","POWER_ACTION_OVERRIDE_APPS","POWER_ACTION_POLICY","POWER_ACTION_POLICY structure","POWER_ACTION_QUERY_ALLOWED","POWER_ACTION_UI_ALLOWED","POWER_FORCE_TRIGGER_RESET","POWER_LEVEL_USER_NOTIFY_EXEC","POWER_LEVEL_USER_NOTIFY_SOUND","POWER_LEVEL_USER_NOTIFY_TEXT","POWER_USER_NOTIFY_BUTTON","POWER_USER_NOTIFY_SHUTDOWN","PPOWER_ACTION_POLICY","PPOWER_ACTION_POLICY structure pointer","_win32_power_action_policy_str","base.power_action_policy_str","winnt/POWER_ACTION_POLICY","winnt/PPOWER_ACTION_POLICY"]
old-location: base\power_action_policy_str.htm
tech.root: base
ms.assetid: 70739f46-54be-4748-8993-ffee3b2a8b6c
ms.date: 12/05/2018
ms.keywords: '*PPOWER_ACTION_POLICY, POWER_ACTION_CRITICAL, POWER_ACTION_DISABLE_WAKES, POWER_ACTION_LIGHTEST_FIRST, POWER_ACTION_LOCK_CONSOLE, POWER_ACTION_OVERRIDE_APPS, POWER_ACTION_POLICY, POWER_ACTION_POLICY structure, POWER_ACTION_QUERY_ALLOWED, POWER_ACTION_UI_ALLOWED, POWER_FORCE_TRIGGER_RESET, POWER_LEVEL_USER_NOTIFY_EXEC, POWER_LEVEL_USER_NOTIFY_SOUND, POWER_LEVEL_USER_NOTIFY_TEXT, POWER_USER_NOTIFY_BUTTON, POWER_USER_NOTIFY_SHUTDOWN, PPOWER_ACTION_POLICY, PPOWER_ACTION_POLICY structure pointer, _win32_power_action_policy_str, base.power_action_policy_str, winnt/POWER_ACTION_POLICY, winnt/PPOWER_ACTION_POLICY'
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
req.typenames: POWER_ACTION_POLICY, *PPOWER_ACTION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PPOWER_ACTION_POLICY
 - winnt/PPOWER_ACTION_POLICY
 - POWER_ACTION_POLICY
 - winnt/POWER_ACTION_POLICY
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
 - POWER_ACTION_POLICY
---

# POWER_ACTION_POLICY structure


## -description

Contains information used to set the system power state.

## -struct-fields

### -field Action

The requested system power state. This member must be one of the 
      <a href="/windows/desktop/api/winnt/ne-winnt-power_action">POWER_ACTION</a> enumeration type values.

### -field Flags

A flag that controls how to switch the power state. This member can be one or more of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_CRITICAL"></a><a id="power_action_critical"></a><dl>
<dt><b>POWER_ACTION_CRITICAL</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Forces a critical suspension.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_DISABLE_WAKES"></a><a id="power_action_disable_wakes"></a><dl>
<dt><b>POWER_ACTION_DISABLE_WAKES</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Disables all wake events.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_LIGHTEST_FIRST"></a><a id="power_action_lightest_first"></a><dl>
<dt><b>POWER_ACTION_LIGHTEST_FIRST</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Uses the first lightest available sleep state.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_LOCK_CONSOLE"></a><a id="power_action_lock_console"></a><dl>
<dt><b>POWER_ACTION_LOCK_CONSOLE</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Requires entry of the system password upon resume from one of the system standby states.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_OVERRIDE_APPS"></a><a id="power_action_override_apps"></a><dl>
<dt><b>POWER_ACTION_OVERRIDE_APPS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Has no effect.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_QUERY_ALLOWED"></a><a id="power_action_query_allowed"></a><dl>
<dt><b>POWER_ACTION_QUERY_ALLOWED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Has no effect.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_ACTION_UI_ALLOWED"></a><a id="power_action_ui_allowed"></a><dl>
<dt><b>POWER_ACTION_UI_ALLOWED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Applications can prompt the user for directions on how to prepare for suspension. Sets bit 0 in the 
        <i>Flags</i> parameter passed in the <i>lParam</i> parameter of 
        <a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>.

</td>
</tr>
</table>

### -field EventCode

The level of user notification. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POWER_FORCE_TRIGGER_RESET"></a><a id="power_force_trigger_reset"></a><dl>
<dt><b>POWER_FORCE_TRIGGER_RESET</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Clears a user power button press.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_LEVEL_USER_NOTIFY_EXEC"></a><a id="power_level_user_notify_exec"></a><dl>
<dt><b>POWER_LEVEL_USER_NOTIFY_EXEC</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Specifies a program to be executed.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_LEVEL_USER_NOTIFY_SOUND"></a><a id="power_level_user_notify_sound"></a><dl>
<dt><b>POWER_LEVEL_USER_NOTIFY_SOUND</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
User notified using sound.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_LEVEL_USER_NOTIFY_TEXT"></a><a id="power_level_user_notify_text"></a><dl>
<dt><b>POWER_LEVEL_USER_NOTIFY_TEXT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
User notified using the UI.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_USER_NOTIFY_BUTTON"></a><a id="power_user_notify_button"></a><dl>
<dt><b>POWER_USER_NOTIFY_BUTTON</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Indicates that the power action is in response to a user power button press.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_USER_NOTIFY_SHUTDOWN"></a><a id="power_user_notify_shutdown"></a><dl>
<dt><b>POWER_USER_NOTIFY_SHUTDOWN</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Indicates a power action of shutdown/off.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_user_power_policy">GLOBAL_USER_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a>



<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>

