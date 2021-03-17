---
UID: NF:powrprof.PowerEnumerate
title: PowerEnumerate function (powrprof.h)
description: Enumerates the specified elements in a power scheme.
helpviewer_keywords: ["ACCESS_INDIVIDUAL_SETTING","ACCESS_SCHEME","ACCESS_SUBGROUP","GUID_BATTERY_SUBGROUP","GUID_DISK_SUBGROUP","GUID_PCIEXPRESS_SETTINGS_SUBGROUP","GUID_PROCESSOR_SETTINGS_SUBGROUP","GUID_SLEEP_SUBGROUP","GUID_SYSTEM_BUTTON_SUBGROUP","GUID_VIDEO_SUBGROUP","NO_SUBGROUP_GUID","PowerEnumerate","PowerEnumerate function","base.powerenumerate","powrprof/PowerEnumerate"]
old-location: base\powerenumerate.htm
tech.root: base
ms.assetid: 5b2c8263-d916-4909-be56-ec784537bdc3
ms.date: 12/05/2018
ms.keywords: ACCESS_INDIVIDUAL_SETTING, ACCESS_SCHEME, ACCESS_SUBGROUP, GUID_BATTERY_SUBGROUP, GUID_DISK_SUBGROUP, GUID_PCIEXPRESS_SETTINGS_SUBGROUP, GUID_PROCESSOR_SETTINGS_SUBGROUP, GUID_SLEEP_SUBGROUP, GUID_SYSTEM_BUTTON_SUBGROUP, GUID_VIDEO_SUBGROUP, NO_SUBGROUP_GUID, PowerEnumerate, PowerEnumerate function, base.powerenumerate, powrprof/PowerEnumerate
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerEnumerate
 - powrprof/PowerEnumerate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerEnumerate
---

# PowerEnumerate function


## -description

Enumerates the specified elements in a power scheme. This function is normally called in a 
    loop incrementing the <i>Index</i> parameter to retrieve subkeys until they've all been 
    enumerated.

## -parameters

### -param RootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param SchemeGuid [in, optional]

The identifier of the power scheme. If this parameter is <b>NULL</b>, 
      an enumeration of the power policies is returned.

### -param SubGroupOfPowerSettingsGuid [in, optional]

The subgroup of power settings.  If this parameter is <b>NULL</b>, an 
      enumeration of settings under the <b>PolicyGuid</b> key is returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NO_SUBGROUP_GUID"></a><a id="no_subgroup_guid"></a><dl>
<dt><b>NO_SUBGROUP_GUID</b></dt>
<dt>fea3413e-7e05-4911-9a71-700331f1c294</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup will be part of the default power scheme.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_DISK_SUBGROUP"></a><a id="guid_disk_subgroup"></a><dl>
<dt><b>GUID_DISK_SUBGROUP</b></dt>
<dt>0012ee47-9041-4b5d-9b77-535fba8b1442</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control power management configuration of the system's hard disk drives.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_SYSTEM_BUTTON_SUBGROUP"></a><a id="guid_system_button_subgroup"></a><dl>
<dt><b>GUID_SYSTEM_BUTTON_SUBGROUP</b></dt>
<dt>4f971e89-eebd-4455-a8de-9e59040e7347</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control configuration of the system power buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_PROCESSOR_SETTINGS_SUBGROUP"></a><a id="guid_processor_settings_subgroup"></a><dl>
<dt><b>GUID_PROCESSOR_SETTINGS_SUBGROUP</b></dt>
<dt>54533251-82be-4824-96c1-47b60b740d00</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control configuration of processor power management features.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_VIDEO_SUBGROUP"></a><a id="guid_video_subgroup"></a><dl>
<dt><b>GUID_VIDEO_SUBGROUP</b></dt>
<dt>7516b95f-f776-4464-8c53-06167f40cc99</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control configuration of the video power management features.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_BATTERY_SUBGROUP"></a><a id="guid_battery_subgroup"></a><dl>
<dt><b>GUID_BATTERY_SUBGROUP</b></dt>
<dt>e73a048d-bf27-4f12-9731-8b2076e8891f</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control battery alarm trip points and actions.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_SLEEP_SUBGROUP"></a><a id="guid_sleep_subgroup"></a><dl>
<dt><b>GUID_SLEEP_SUBGROUP</b></dt>
<dt>238C9FA8-0AAD-41ED-83F4-97BE242C8F20</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control system sleep settings.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_PCIEXPRESS_SETTINGS_SUBGROUP"></a><a id="guid_pciexpress_settings_subgroup"></a><dl>
<dt><b>GUID_PCIEXPRESS_SETTINGS_SUBGROUP</b></dt>
<dt>501a4d13-42af-4429-9fd1-a8218c268e20</dt>
</dl>
</td>
<td width="60%">
Settings in this subgroup control PCI Express settings.

</td>
</tr>
</table>

### -param AccessFlags [in]

A set of flags that specifies what will be enumerated

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_SCHEME"></a><a id="access_scheme"></a><dl>
<dt><b>ACCESS_SCHEME</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Enumerate power schemes. The <i>SchemeGuid</i> and 
        <i>SubgroupOfPowerSettingsGuid</i> parameters will be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_SUBGROUP"></a><a id="access_subgroup"></a><dl>
<dt><b>ACCESS_SUBGROUP</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
Enumerate subgroups under <i>SchemeGuid</i>. The 
        <i>SubgroupOfPowerSettingsGuid</i> parameter will be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_INDIVIDUAL_SETTING"></a><a id="access_individual_setting"></a><dl>
<dt><b>ACCESS_INDIVIDUAL_SETTING</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
Enumerate individual power settings under 
        <i>SchemeGuid</i>&#92;<i>SubgroupOfPowerSettingsGuid</i>. To enumerate power 
        settings directly under the <i>SchemeGuid</i> key, use 
        <b>NO_SUBGROUP_GUID</b> as the <i>SubgroupOfPowerSettingsGuid</i> 
        parameter.

</td>
</tr>
</table>

### -param Index [in]

The zero-based index of the scheme, subgroup, or setting that is being enumerated.

### -param Buffer [out, optional]

A pointer to a variable to receive the elements. If this parameter is <b>NULL</b>, the function retrieves the size of the buffer required.

### -param BufferSize [in, out]

A pointer to a variable that on input contains the size of the buffer pointed to by 
      the <i>Buffer</i> parameter. If the  <i>Buffer</i> parameter is 
      <b>NULL</b> or if the <i>BufferSize</i> is not large enough, the function 
      will return <b>ERROR_MORE_DATA</b> and the variable receives the required buffer size.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed. If the buffer size passed in the <i>BufferSize</i> parameter is too small, 
      or if the <i>Buffer</i> parameter is <b>NULL</b>, 
      <b>ERROR_MORE_DATA</b> will be returned and the <b>DWORD</b> pointed to 
      by the <i>BufferSize</i> parameter will be filled in with the required buffer size.

## -see-also

<a href="/windows/desktop/api/powrprof/ne-powrprof-power_data_accessor">POWER_DATA_ACCESSOR</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>