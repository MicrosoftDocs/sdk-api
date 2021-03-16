---
UID: NF:powrprof.PowerReadPossibleFriendlyName
title: PowerReadPossibleFriendlyName function (powrprof.h)
description: Retrieves the friendly name for one of the possible choices of a power setting value.
helpviewer_keywords: ["GUID_BATTERY_SUBGROUP","GUID_DISK_SUBGROUP","GUID_PCIEXPRESS_SETTINGS_SUBGROUP","GUID_PROCESSOR_SETTINGS_SUBGROUP","GUID_SLEEP_SUBGROUP","GUID_SYSTEM_BUTTON_SUBGROUP","GUID_VIDEO_SUBGROUP","NO_SUBGROUP_GUID","PowerReadPossibleFriendlyName","PowerReadPossibleFriendlyName function","base.powerreadpossiblefriendlyname","powrprof/PowerReadPossibleFriendlyName"]
old-location: base\powerreadpossiblefriendlyname.htm
tech.root: base
ms.assetid: 38f3c5f4-ec65-47f0-b15c-36cd2b1e2813
ms.date: 12/05/2018
ms.keywords: GUID_BATTERY_SUBGROUP, GUID_DISK_SUBGROUP, GUID_PCIEXPRESS_SETTINGS_SUBGROUP, GUID_PROCESSOR_SETTINGS_SUBGROUP, GUID_SLEEP_SUBGROUP, GUID_SYSTEM_BUTTON_SUBGROUP, GUID_VIDEO_SUBGROUP, NO_SUBGROUP_GUID, PowerReadPossibleFriendlyName, PowerReadPossibleFriendlyName function, base.powerreadpossiblefriendlyname, powrprof/PowerReadPossibleFriendlyName
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
 - PowerReadPossibleFriendlyName
 - powrprof/PowerReadPossibleFriendlyName
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
 - PowerReadPossibleFriendlyName
---

# PowerReadPossibleFriendlyName function


## -description

Retrieves the friendly name for one of the possible choices of a power setting value.

## -parameters

### -param RootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param SubGroupOfPowerSettingsGuid [in, optional]

The subgroup of power settings. This parameter can be one of the following values defined in WinNT.h. Use <b>NO_SUBGROUP_GUID</b> to refer to the 
      default power scheme.

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
Settings in this subgroup are part of the default power scheme.

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

### -param PowerSettingGuid [in, optional]

The identifier of the power setting.

### -param PossibleSettingIndex [in]

The zero-based index for the possible setting.

### -param Buffer [out, optional]

A pointer to a buffer that receives the friendly name. If this parameter is <b>NULL</b>, the <i>BufferSize</i> 
parameter receives the required buffer size. The strings returned are all wide (Unicode) strings.

### -param BufferSize [in, out]

A pointer to a variable that contains the size of the buffer pointed to by the 
<i>Buffer</i> parameter. 

If the <i>Buffer</i> parameter is <b>NULL</b>, the function returns ERROR_SUCCESS and the variable receives the required buffer size. 

If the specified buffer size is not large enough to hold the requested data, the function returns <b>ERROR_MORE_DATA</b> and the variable receives the required buffer size.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if the call failed. If the buffer size specified by the <i>BufferSize</i> parameter is too small, 
	      
<b>ERROR_MORE_DATA</b> will be returned and the <b>DWORD</b> pointed to by the <i>BufferSize</i> parameter will be filled in with the required buffer size.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>