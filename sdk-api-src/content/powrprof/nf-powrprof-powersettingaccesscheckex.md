---
UID: NF:powrprof.PowerSettingAccessCheckEx
title: PowerSettingAccessCheckEx function (powrprof.h)
description: Queries for a group policy override for specified power settings and specifies the requested access for the setting.
helpviewer_keywords: ["ACCESS_ACTIVE_SCHEME","ACCESS_AC_POWER_SETTING_INDEX","ACCESS_CREATE_SCHEME","ACCESS_DC_POWER_SETTING_INDEX","ACCESS_SCHEME","KEY_READ","KEY_WRITE","PowerSettingAccessCheckEx","PowerSettingAccessCheckEx function","base.powersettingaccesscheckex","powrprof/PowerSettingAccessCheckEx"]
old-location: base\powersettingaccesscheckex.htm
tech.root: base
ms.assetid: dad9cca9-5961-48b5-b7d0-4828eca3364b
ms.date: 12/05/2018
ms.keywords: ACCESS_ACTIVE_SCHEME, ACCESS_AC_POWER_SETTING_INDEX, ACCESS_CREATE_SCHEME, ACCESS_DC_POWER_SETTING_INDEX, ACCESS_SCHEME, KEY_READ, KEY_WRITE, PowerSettingAccessCheckEx, PowerSettingAccessCheckEx function, base.powersettingaccesscheckex, powrprof/PowerSettingAccessCheckEx
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerSettingAccessCheckEx
 - powrprof/PowerSettingAccessCheckEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
api_name:
 - PowerSettingAccessCheckEx
---

# PowerSettingAccessCheckEx function


## -description

Queries for a group policy override for specified power settings and specifies the requested access for the setting.

## -parameters

### -param AccessFlags [in]

The type of access to check for group policy overrides.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_AC_POWER_SETTING_INDEX"></a><a id="access_ac_power_setting_index"></a><dl>
<dt><b>ACCESS_AC_POWER_SETTING_INDEX</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
Check for overrides on AC power settings.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DC_POWER_SETTING_INDEX"></a><a id="access_dc_power_setting_index"></a><dl>
<dt><b>ACCESS_DC_POWER_SETTING_INDEX</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Check for overrides on DC power settings.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_SCHEME"></a><a id="access_scheme"></a><dl>
<dt><b>ACCESS_SCHEME</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on specific power schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ACTIVE_SCHEME"></a><a id="access_active_scheme"></a><dl>
<dt><b>ACCESS_ACTIVE_SCHEME</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on active power schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_CREATE_SCHEME"></a><a id="access_create_scheme"></a><dl>
<dt><b>ACCESS_CREATE_SCHEME</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on creating or restoring power schemes.

</td>
</tr>
</table>

### -param PowerGuid [in, optional]

The identifier of the power setting.

### -param AccessType [in]

The type of security access for the setting. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KEY_READ"></a><a id="key_read"></a><dl>
<dt><b>KEY_READ</b></dt>
</dl>
</td>
<td width="60%">
Combines the STANDARD_RIGHTS_READ, KEY_QUERY_VALUE, KEY_ENUMERATE_SUB_KEYS, and KEY_NOTIFY values.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_WRITE"></a><a id="key_write"></a><dl>
<dt><b>KEY_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Combines the STANDARD_RIGHTS_WRITE, KEY_SET_VALUE, and KEY_CREATE_SUB_KEY access rights.

</td>
</tr>
</table>

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The specified power setting is not currently overridden by a group policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
<dt>1260 (0x4EC)</dt>
</dl>
</td>
<td width="60%">
This program is blocked by group policy. For more information, contact your system administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_REMOTE_DISALLOWED</b></dt>
<dt>1640 (0x668)</dt>
</dl>
</td>
<td width="60%">
Only Administrators can remotely access power settings.

</td>
</tr>
</table>