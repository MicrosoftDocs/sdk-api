---
UID: NF:winuser.QueryDisplayConfig
title: QueryDisplayConfig function (winuser.h)
description: The QueryDisplayConfig function retrieves information about all possible display paths for all display devices, or views, in the current setting.
helpviewer_keywords: ["CCD_Functions_4fc57ba2-e10b-4d28-bbaf-a5ded2264e59.xml","QueryDisplayConfig","QueryDisplayConfig function [Display Devices]","display.querydisplayconfig","winuser/QueryDisplayConfig"]
old-location: display\querydisplayconfig.htm
tech.root: display
ms.assetid: b1792d7f-f216-4250-a6b6-a11b251a9cec
ms.date: 12/05/2018
ms.keywords: CCD_Functions_4fc57ba2-e10b-4d28-bbaf-a5ded2264e59.xml, QueryDisplayConfig, QueryDisplayConfig function [Display Devices], display.querydisplayconfig, winuser/QueryDisplayConfig
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib; OneCoreUAP.lib on Windows 10
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryDisplayConfig
 - winuser/QueryDisplayConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-SysParams-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-SysParams-l1-1-0.dll
 - MinUser.dll
api_name:
 - QueryDisplayConfig
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# QueryDisplayConfig function


## -description

The <b>QueryDisplayConfig</b> function retrieves information about all possible display paths for all display devices, or views, in the current setting.

## -parameters

### -param flags [in]

The type of information to retrieve. The value for the <i>Flags</i> parameter must use one of the following values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QDC_ALL_PATHS"></a><a id="qdc_all_paths"></a><dl>
<dt><b>QDC_ALL_PATHS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Returns all the possible path combinations of sources to targets.

> [!NOTE]
> In the case of any temporary modes, the QDC_ALL_PATHS setting means the mode data returned may not be the same as that which is stored in the persistence database.

> [!NOTE]
> This flag may be very expensive to compute. It's not recommended to use this flag unless the caller is trying to determine the set of valid connections between sources and targets.

</td>
</tr>
<tr>
<td width="40%"><a id="QDC_ONLY_ACTIVE_PATHS"></a><a id="qdc_only_active_paths"></a><dl>
<dt><b>QDC_ONLY_ACTIVE_PATHS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns currently active paths only.    

> [!NOTE]
> In the case of any temporary modes, the QDC_ONLY_ACTIVE_PATHS setting means the mode data returned may not be the same as that which is stored in the persistence database.

</td>
</tr>
<tr>
<td width="40%"><a id="QDC_DATABASE_CURRENT"></a><a id="qdc_database_current"></a><dl>
<dt><b>QDC_DATABASE_CURRENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Returns active paths as defined in the CCD database for the currently connected displays.
</td>
</tr>
</table>

The _Flags_ parameter may also be bitwise OR'ed with zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QDC_VIRTUAL_MODE_AWARE"></a><a id="qdc_virtual_mode_aware"></a><dl>
<dt><b>QDC_VIRTUAL_MODE_AWARE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
This flag should be bitwise OR'ed with other flags to indicate that the caller is aware of virtual mode support.

Supported starting in Windows 10.
</td>
</tr>
<tr>
<td width="40%"><a id="QDC_INCLUDE_HMD"></a><a id="qdc_include_hmd"></a><dl>
<dt><b>QDC_INCLUDE_HMD</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
This flag should be bitwise OR'ed with QDC_ONLY_ACTIVE_PATHS to indicate that the caller would like to include head-mounted displays (HMDs) in the list of active paths. See Remarks for more information.

Supported starting in Windows 10 1703 Creators Update.
</td>
</tr>
<tr>
<td width="40%"><a id="QDC_VIRTUAL_REFRESH_RATE_AWARE"></a><a id="qdc_virtual_refresh_rate_aware"></a><dl>
<dt><b>QDC_VIRTUAL_REFRESH_RATE_AWARE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
This flag should be bitwise OR'ed with other flags to indicate that the caller is aware of virtual refresh rate support.

Supported starting in Windows 11.
</td>
</tr>
</table>

### -param numPathArrayElements [in, out]

Pointer to a variable that contains the number of elements in <i>pPathInfoArray</i>. This parameter cannot be <b>NULL</b>. If <b>QueryDisplayConfig</b> returns ERROR_SUCCESS, <i>pNumPathInfoElements</i> is updated with the number of valid entries in <i>pPathInfoArray</i>.

### -param pathArray [out]

Pointer to a variable that contains an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a> elements. Each element in <i>pPathInfoArray</i> describes a single path from a source to a target. The source and target mode information indexes are only valid in combination with the <i>pmodeInfoArray</i> tables that are returned for the API at the same time. This parameter cannot be <b>NULL</b>. The <i>pPathInfoArray</i> is always returned in path priority order. For more information about path priority order, see <a href="/windows-hardware/drivers/display/path-priority-order">Path Priority Order</a>.

### -param numModeInfoArrayElements [in, out]

Pointer to a variable that specifies the number in element of the mode information table. This parameter cannot be <b>NULL</b>. If <b>QueryDisplayConfig</b> returns ERROR_SUCCESS, <i>pNumModeInfoArrayElements</i> is updated with the number of valid entries in <i>pModeInfoArray</i>.

### -param modeInfoArray [out]

Pointer to a variable that contains an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a> elements. This parameter cannot be <b>NULL</b>.

### -param currentTopologyId [out, optional]

Pointer to a variable that receives the identifier of the currently active topology in the CCD database. For a list of possible values, see the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_topology_id">DISPLAYCONFIG_TOPOLOGY_ID</a> enumerated type.

The <i>pCurrentTopologyId</i> parameter is only set when the <i>Flags</i> parameter value is QDC_DATABASE_CURRENT.

If the <i>Flags</i> parameter value is set to QDC_DATABASE_CURRENT, the <i>pCurrentTopologyId</i> parameter must not be <b>NULL</b>. If the <i>Flags</i> parameter value is not set to QDC_DATABASE_CURRENT, the <i>pCurrentTopologyId</i> parameter value must be <b>NULL</b>.

## -returns

The function returns one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The combination of parameters and flags that are specified is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The system is not running a graphics driver that was written according to the <a href="/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide">Windows Display Driver Model (WDDM)</a>. The function is only supported on a system with a WDDM driver running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the console session. This error occurs if the calling process does not have access to the current desktop or is running on a remote session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The supplied path and mode buffer are too small.

</td>
</tr>
</table>

## -remarks

As the <a href="/windows/desktop/api/winuser/nf-winuser-getdisplayconfigbuffersizes">GetDisplayConfigBufferSizes</a> function can only determine the required array size at a particular moment in time, it is possible that between calls to <b>GetDisplayConfigBufferSizes</b> and <b>QueryDisplayConfig</b> the system configuration will change and the provided array sizes will no longer be sufficient to store the new path data. In this situation, <b>QueryDisplayConfig</b> fails with ERROR_INSUFFICIENT_BUFFER, and the caller should call <b>GetDisplayConfigBufferSizes</b> again to get the new array sizes. The caller should then allocate the correct amount of memory. 

<b>QueryDisplayConfig</b> returns paths in the path array that the <i>pPathInfoArray</i> parameter specifies and the source and target modes in the mode array that the <i>pModeInfoArray</i> parameter specifies. <b>QueryDisplayConfig</b> always returns paths in path priority order. If QDC_ALL_PATHS is set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> returns all the inactive paths after the active paths. 

Full path, source mode, and target mode information is available for all active paths. The <b>ModeInfoIdx</b> members in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structures for the source and target are set up for these active paths. For inactive paths, returned source and target mode information is not available; therefore, the target information in the path structure is set to default values, and the source and target mode indexes are marked as invalid. For database queries, if the current connect monitors have an entry, <b>QueryDisplayConfig</b> returns full path, source mode, and target mode information (same as for active paths). However, if the database does not have a entry, <b>QueryDisplayConfig</b> returns just the path information with the default target details (same as for inactive paths). 

For an example of how source and target mode information relates to path information, see <a href="/windows-hardware/drivers/display/relationship-of-mode-information-to-path-information">Relationship of Mode Information to Path Information</a>.

The caller can use <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> to obtain additional information about the source or target device, for example, the monitor names and monitor preferred mode and source device name.

If a target is currently being force projected, the <b>statusFlags</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure has one of the DISPLAYCONFIG_TARGET_FORCED_XXX flags set. 

If the QDC_DATABASE_CURRENT flag is set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> returns the topology identifier of the active database topology in the variable that the <i>pCurrentTopologyId</i> parameter points to. If the QDC_ALL_PATHS or QDC_ONLY_ACTIVE_PATHS flag is set in the <i>Flags</i> parameter, the <i>pCurrentTopologyId</i> parameter must be set to <b>NULL</b>; otherwise, <b>QueryDisplayConfig</b> returns ERROR_INVALID_PARAMETER.

If a caller calls <b>QueryDisplayConfig</b> with the QDC_DATABASE_CURRENT flag set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> initializes the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_2dregion">DISPLAYCONFIG_2DREGION</a> structure that is specified in the <b>totalSize</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> structure to zeros and does not complete DISPLAYCONFIG_2DREGION.

The DEVMODE structure that is returned by the <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a> Win32 function (described in the Windows SDK documentation) contains information that relates to both the source and target modes. However, the <a href="/windows-hardware/drivers/display/ccd-apis">CCD APIs</a> explicitly separate the source and target mode components.

### Head-mounted and specialized monitors

__QueryDisplayConfig__ and many other Win32 display APIs have limited awareness of head-mounted and specialized monitors, since those displays do not participate in the Windows desktop environment. However, there are scenarios where it's necessary to understand the connectivity of these displays (e.g. content protection scenarios). For these limited scenarios, `(QDC_INCLUDE_HMD | QDC_ONLY_ACTIVE_PATHS)` can be used to discover the connectivity of head-mounted displays. These paths will be marked with the the DISPLAYCONFIG_TARGET_IS_HMD flag in the [DISPLAYCONFIG_PATH_TARGET_INFO.statusFlags](../wingdi/ns-wingdi-displayconfig_path_target_info) field. This support was added in the Windows 10 1703 Creators Update.

### <a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI virtualization
This API does not participate in DPI virtualization. All sizes in the DEVMODE structure are in terms of physical pixels, and are not related to the calling context.

## Examples

The following example enumerates active display paths with __QueryDisplayConfig__ and __GetDisplayConfigBufferSizes__ and prints out data for each path using __DisplayConfigGetDeviceInfo__.

```cpp
#include <windows.h>
#include <vector>
#include <iostream>
#include <string>

using namespace std;

int main()
{
    vector<DISPLAYCONFIG_PATH_INFO> paths;
    vector<DISPLAYCONFIG_MODE_INFO> modes;
    UINT32 flags = QDC_ONLY_ACTIVE_PATHS | QDC_VIRTUAL_MODE_AWARE;
    LONG result = ERROR_SUCCESS;

    do
    {
        // Determine how many path and mode structures to allocate
        UINT32 pathCount, modeCount;
        result = GetDisplayConfigBufferSizes(flags, &pathCount, &modeCount);

        if (result != ERROR_SUCCESS)
        {
            return HRESULT_FROM_WIN32(result);
        }

        // Allocate the path and mode arrays
        paths.resize(pathCount);
        modes.resize(modeCount);

        // Get all active paths and their modes
        result = QueryDisplayConfig(flags, &pathCount, paths.data(), &modeCount, modes.data(), nullptr);

        // The function may have returned fewer paths/modes than estimated
        paths.resize(pathCount);
        modes.resize(modeCount);

        // It's possible that between the call to GetDisplayConfigBufferSizes and QueryDisplayConfig
        // that the display state changed, so loop on the case of ERROR_INSUFFICIENT_BUFFER.
    } while (result == ERROR_INSUFFICIENT_BUFFER);

    if (result != ERROR_SUCCESS)
    {
        return HRESULT_FROM_WIN32(result);
    }

    // For each active path
    for (auto& path : paths)
    {
        // Find the target (monitor) friendly name
        DISPLAYCONFIG_TARGET_DEVICE_NAME targetName = {};
        targetName.header.adapterId = path.targetInfo.adapterId;
        targetName.header.id = path.targetInfo.id;
        targetName.header.type = DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME;
        targetName.header.size = sizeof(targetName);
        result = DisplayConfigGetDeviceInfo(&targetName.header);

        if (result != ERROR_SUCCESS)
        {
            return HRESULT_FROM_WIN32(result);
        }

        // Find the adapter device name
        DISPLAYCONFIG_ADAPTER_NAME adapterName = {};
        adapterName.header.adapterId = path.targetInfo.adapterId;
        adapterName.header.type = DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME;
        adapterName.header.size = sizeof(adapterName);

        result = DisplayConfigGetDeviceInfo(&adapterName.header);

        if (result != ERROR_SUCCESS)
        {
            return HRESULT_FROM_WIN32(result);
        }

        wcout
            << L"Monitor with name "
            << (targetName.flags.friendlyNameFromEdid ? targetName.monitorFriendlyDeviceName : L"Unknown")
            << L" is connected to adapter "
            << adapterName.adapterDevicePath
            << L" on target "
            << path.targetInfo.id
            << L"\n";
    }
}
```

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_topology_id">DISPLAYCONFIG_TOPOLOGY_ID</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
