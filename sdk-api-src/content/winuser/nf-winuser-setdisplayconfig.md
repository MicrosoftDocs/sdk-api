---
UID: NF:winuser.SetDisplayConfig
title: SetDisplayConfig function (winuser.h)
description: The SetDisplayConfig function modifies the display topology, source, and target modes by exclusively enabling the specified paths in the current session.
helpviewer_keywords: ["CCD_Functions_fceeecb0-8c34-4ff0-b201-fc5b7f39f2df.xml","SetDisplayConfig","SetDisplayConfig function [Display Devices]","display.setdisplayconfig","winuser/SetDisplayConfig"]
old-location: display\setdisplayconfig.htm
tech.root: display
ms.assetid: 9f649fa0-ffb2-44c6-9a66-049f888e3b04
ms.date: 12/05/2018
ms.keywords: CCD_Functions_fceeecb0-8c34-4ff0-b201-fc5b7f39f2df.xml, SetDisplayConfig, SetDisplayConfig function [Display Devices], display.setdisplayconfig, winuser/SetDisplayConfig
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of the Windows operating systems.
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDisplayConfig
 - winuser/SetDisplayConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-SysParams-l1-1-0.dll
 - MinUser.dll
api_name:
 - SetDisplayConfig
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetDisplayConfig function


## -description

The <b>SetDisplayConfig</b> function modifies the display topology, source, and target modes by exclusively enabling the specified paths in the current session.

## -parameters

### -param numPathArrayElements [in]

Number of elements in <i>pathArray</i>.

### -param pathArray [in, optional]

Array of all display paths that are to be set. Only the paths within this array that have the DISPLAYCONFIG_PATH_ACTIVE flag set in the <b>flags</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a> are set. This parameter can be <b>NULL</b>. The order in which active paths appear in this array determines the path priority. For more information about path priority order, see <a href="/windows-hardware/drivers/display/path-priority-order">Path Priority Order</a>.

### -param numModeInfoArrayElements [in]

Number of elements in <i>modeInfoArray</i>.

### -param modeInfoArray [in, optional]

Array of display source and target mode information (<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a>) that is referenced by the <b>modeInfoIdx</b> member of DISPLAYCONFIG_PATH_SOURCE_INFO and DISPLAYCONFIG_PATH_TARGET_INFO element of path information from <i>pathArray</i>. This parameter can be <b>NULL</b>.

### -param flags [in]

A bitwise OR of flag values that indicates the behavior of this function. This parameter can be one the following values, or a combination of the following values; 0 is not valid. See below for a description of valid flag combinations.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SDC_APPLY"></a><a id="sdc_apply"></a><dl>
<dt><b>SDC_APPLY</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The resulting topology, source, and target mode is set.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_NO_OPTIMIZATION"></a><a id="sdc_no_optimization"></a><dl>
<dt><b>SDC_NO_OPTIMIZATION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
A modifier to the SDC_APPLY flag. This causes the change mode to be forced all the way down to the driver for each active display.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_USE_SUPPLIED_DISPLAY_CONFIG"></a><a id="sdc_use_supplied_display_config"></a><dl>
<dt><b>SDC_USE_SUPPLIED_DISPLAY_CONFIG</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The topology, source, and target mode information that are supplied in the <i>pathArray</i> and the <i>modeInfoArray</i> parameters are used, rather than looking up the configuration in the database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_SAVE_TO_DATABASE"></a><a id="sdc_save_to_database"></a><dl>
<dt><b>SDC_SAVE_TO_DATABASE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The resulting topology, source, and target mode are saved to the database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_VALIDATE"></a><a id="sdc_validate"></a><dl>
<dt><b>SDC_VALIDATE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The system tests for the requested topology, source, and target mode information to determine whether it can be set. 
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_ALLOW_CHANGES"></a><a id="sdc_allow_changes"></a><dl>
<dt><b>SDC_ALLOW_CHANGES</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If required, the function can modify the specified source and target mode information in order to create a functional display path set.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_TOPOLOGY_CLONE"></a><a id="sdc_topology_clone"></a><dl>
<dt><b>SDC_TOPOLOGY_CLONE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The caller requests the last clone configuration from the persistence database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_TOPOLOGY_EXTEND"></a><a id="sdc_topology_extend"></a><dl>
<dt><b>SDC_TOPOLOGY_EXTEND</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The caller requests the last extended configuration from the persistence database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_TOPOLOGY_INTERNAL"></a><a id="sdc_topology_internal"></a><dl>
<dt><b>SDC_TOPOLOGY_INTERNAL</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The caller requests the last internal configuration from the persistence database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_TOPOLOGY_EXTERNAL"></a><a id="sdc_topology_external"></a><dl>
<dt><b>SDC_TOPOLOGY_EXTERNAL</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The caller requests the last external configuration from the persistence database.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_TOPOLOGY_SUPPLIED"></a><a id="sdc_topology_supplied"></a><dl>
<dt><b>SDC_TOPOLOGY_SUPPLIED</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The caller provides the path data so the function only queries the persistence database to find and use the source and target mode.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_USE_DATABASE_CURRENT"></a><a id="sdc_use_database_current"></a><dl>
<dt><b>SDC_USE_DATABASE_CURRENT</b></dt>
<dt>(SDC_TOPOLOGY_INTERNAL | SDC_TOPOLOGY_CLONE | SDC_TOPOLOGY_EXTEND | SDC_TOPOLOGY_EXTERNAL)</dt>
</dl>
</td>
<td width="60%">
The caller requests a combination of all four SDC_TOPOLOGY_XXX configurations. This value informs the API to set the last known display configuration for the current connected monitors.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_PATH_PERSIST_IF_REQUIRED"></a><a id="sdc_path_persist_if_required"></a><dl>
<dt><b>SDC_PATH_PERSIST_IF_REQUIRED</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
When the function processes a SDC_TOPOLOGY_XXX request, it can force path persistence on a target to satisfy the request if necessary. For information about the other flags that this flag can be combined with, see the following list. 
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_FORCE_MODE_ENUMERATION"></a><a id="sdc_force_mode_enumeration"></a><dl>
<dt><b>SDC_FORCE_MODE_ENUMERATION</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The caller requests that the driver is given an opportunity to update the GDI mode list while <b>SetDisplayConfig</b> sets the new display configuration. This flag value is only valid when the SDC_USE_SUPPLIED_DISPLAY_CONFIG and SDC_APPLY flag values are also specified. 
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_ALLOW_PATH_ORDER_CHANGES"></a><a id="sdc_allow_path_order_changes"></a><dl>
<dt><b>SDC_ALLOW_PATH_ORDER_CHANGES</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
A modifier to the SDC_TOPOLOGY_SUPPLIED flag that indicates that <b>SetDisplayConfig</b> should ignore the path order of the supplied topology when searching the database. When this flag is set, the topology set is the most recent topology that contains all the paths regardless of the path order. 
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_VIRTUAL_MODE_AWARE"></a><a id="sdc_virtual_mode_aware"></a><dl>
<dt><b>SDC_VIRTUAL_MODE_AWARE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
A modifier to the SDC_USE_SUPPLIED_DISPLAY_CONFIG and SDC_TOPOLOGY_SUPPLIED flags that the caller is aware of virtual modes.
Supported starting in Windows 10.
</td>
</tr>
<tr>
<td width="40%"><a id="SDC_VIRTUAL_REFRESH_RATE_AWARE"></a><a id="sdc_virtual_refresh_rate_aware"></a><dl>
<dt><b>SDC_VIRTUAL_REFRESH_RATE_AWARE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
A modifier to the SDC_USE_SUPPLIED_DISPLAY_CONFIG and SDC_TOPOLOGY_SUPPLIED flags that the caller is aware of virtual refresh rates.
Supported starting in Windows 11.
</td>
</tr>
</table>

The following list contains valid combinations of values for the <i>Flags</i> parameter: 

<ul>
<li>
Either SDC_APPLY or SDC_VALIDATE must be set, but not both. 

</li>
<li>
Either SDC_USE_SUPPLIED_DISPLAY_CONFIG or any combinations of SDC_TOPOLOGY_XXX must be set. SDC_USE_SUPPLIED_DISPLAY_CONFIG cannot be set with any SDC_TOPOLOGY_XXX flag. 

</li>
<li>
SDC_NO_OPTIMIZATION can only be set with SDC_APPLY. 

</li>
<li>
SDC_ALLOW_CHANGES is allowed with any other valid combination. 

</li>
<li>
SDC_SAVE_TO_DATABASE can only be set with SDC_USE_SUPPLIED_DISPLAY_CONFIG. 

</li>
<li>
SDC_PATH_PERSIST_IF_REQUIRED cannot be used with SDC_USE_SUPPLIED_DISPLAY_CONFIG or SDC_TOPOLOGY_SUPPLIED. 

</li>
<li>
SDC_FORCE_MODE_ENUMERATION is only valid when SDC_APPLY and SDC_USE_SUPPLIED_DISPLAY_CONFIG are specified. 

</li>
<li>
SDC_ALLOW_PATH_ORDER_CHANGES is allowed only when SDC_TOPOLOGY_SUPPLIED is specified. 

</li>
<li>
SDC_TOPOLOGY_SUPPLIED cannot be used with any other SDC_TOPOLOGY_XXX flag. Because of a validation issue, if a caller violates this rule, <b>SetDisplayConfig</b> does not fail. However, <b>SetDisplayConfig</b> ignores the SDC_TOPOLOGY_SUPPLIED flag.

</li>
</ul>
SDC_TOPOLOGY_XXX flags can be used in combinations. For example, if SDC_TOPOLOGY_CLONE and SDC_TOPOLOGY_EXTEND are set, the API uses the most recent clone or extend topology, which every topology was set with most recently for the current connected monitors.

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
The combination of parameters and flags specified is invalid.

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
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The function could not find a workable solution for the source and target modes that the caller did not specify.

</td>
</tr>
</table>

## -remarks

The <b>SetDisplayConfig</b> function takes the active display paths with any specified source and target mode information and uses best mode logic to generate any missing source and target mode information. This function then sets the complete display path.

The <b>ModeInfoIdx</b> members in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structures are used to indicate whether source and target mode are supplied for a given active path. If the index value is DISPLAYCONFIG_PATH_MODE_IDX_INVALID for either, this indicates the mode information is not being specified. It is valid for the path plus source mode or the path plus source and target mode information to be specified for a given path. However, it is not valid for the path plus target mode to be specified without the source mode.

The source and target modes for each source and target identifiers can only appear in the <i>modeInfoArray</i> array once. For example, a source mode for source identifier S1 can only appear in the table once; if multiple paths reference the same source, they have to use the same <b>ModeInfoIdx</b>.

The expectation is that most callers use <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to get the current configuration along with other valid possibilities and then use <b>SetDisplayConfig</b> to test and set the configuration.

The order in which the active paths appear in the <i>PathArray</i> array determines the path priority.

By default, <b>SetDisplayConfig</b> never changes any supplied path, source mode, or target mode information. If best mode logic cannot find a solution without changing the specified display path information, <b>SetDisplayConfig</b> fails with ERROR_BAD_CONFIGURATION. In this case, the caller should specify the SDC_ALLOW_CHANGES flag to allow the function to tweak some of the specified source and mode details to allow the display path change to be successful.

If the specified or calculated source and target modes have the same dimensions, <b>SetDisplayConfig</b> automatically sets the path scaling to DISPLAYCONFIG_PPR_IDENTITY before setting the display path and saving it in the database. For information about how <b>SetDisplayConfig</b> handles scaling, see <a href="/windows-hardware/drivers/display/scaling-the-desktop-image">Scaling the Desktop Image</a>.

When the caller specifies the SDC_USE_SUPPLIED_DISPLAY_CONFIG flag to set a clone path and if any source mode indexes are invalid in the path array, <b>SetDisplayConfig</b> determines that all of the source mode indexes from that source are invalid. <b>SetDisplayConfig</b> uses the best mode logic to determine the source mode information. 

Except for the SDC_TOPOLOGY_SUPPLIED flag (for more information about SDC_TOPOLOGY_SUPPLIED, see the following paragraph), the SDC_TOPOLOGY_XXX flags set last display path settings, including the source and target mode information for that topology type. For information about valid SDC_TOPOLOGY_XXX flag combinations, see the <i>Flags</i> parameter description. The <i>pathArray</i> and <i>modeInfoArray</i> parameters must be <b>NULL</b>, and their associated sizes must be zero. For example, if SDC_TOPOLOGY_CLONE and SDC_TOPOLOGY_EXTEND are set, this function uses the most recent clone or extend display path configuration. If a single topology type is requested, the last configuration of that type is used. If that topology had never been set before, <b>SetDisplayConfig</b> uses the best topology logic to find the best topology, and then best mode logic to find the best source and target mode to use. If a combination of the topology flags had been set and none of them had database entries, the following priority is used. For laptops: clone, extend, internal, and then external; for desktops the priority is extend and then clone.

The caller can specify the SDC_TOPOLOGY_SUPPLIED flag to indicate that it sets just the path information (topology) and requests that <b>SetDisplayConfig</b> obtains and then uses the source and target mode information from the persistence database. If the active paths that the caller supplies do not have an entry in the persistence database, <b>SetDisplayConfig</b> fails. In this case, if the caller calls <b>SetDisplayConfig</b> again with the same path data but with the SDC_USE_SUPPLIED_DISPLAY_CONFIG flag set, <b>SetDisplayConfig</b> uses best mode logic to create the source and target mode information. When the caller specifies SDC_TOPOLOGY_SUPPLIED, the caller must set the <i>numModeInfoArrayElements</i> parameter to zero and the <i>modeInfoArray</i> parameter to <b>NULL</b>; however, the caller must set the <i>pathArray</i> and <i>numPathArrayElements</i> parameters for the path information that the caller requires. The caller must mark all the source and target mode indexes as invalid (DISPLAYCONFIG_PATH_MODE_IDX_INVALID) in this path data. 

The following table provides some common scenarios where <b>SetDisplayConfig</b> is called along with the flag combinations that the caller passes to the <i>Flags</i> parameter to achieve the scenarios.

<table>
<tr>
<th>Scenario</th>
<th>Flag combination</th>
</tr>
<tr>
<td>
Test whether a specified display configuration is supported on the computer

</td>
<td>
SDC_VALIDATE | SDC_USE_SUPPLIED_DISPLAY_CONFIG

</td>
</tr>
<tr>
<td>
Set a specified display configuration and save to the database

</td>
<td>
SDC_APPLY | SDC_USE_SUPPLIED_DISPLAY_CONFIG | SDC_SAVE_TO_DATABASE

</td>
</tr>
<tr>
<td>
Set a temporary display configuration (that is, the display configuration will not be saved)

</td>
<td>
SDC_APPLY | SDC_USE_SUPPLIED_DISPLAY_CONFIG

</td>
</tr>
<tr>
<td>
Test whether clone is supported on the computer

</td>
<td>
SDC_VALIDATE | SDC_TOPOLOGY_CLONE

</td>
</tr>
<tr>
<td>
Set clone topology

</td>
<td>
SDC_APPLY | SDC_TOPOLOGY_CLONE

</td>
</tr>
<tr>
<td>
Set clone topology and allow path persistence to be enabled if required to satisfy the request

</td>
<td>
SDC_APPLY | SDC_TOPOLOGY_CLONE | SDC_PATH_PERSIST_IF_REQUIRED

</td>
</tr>
<tr>
<td>
Return from a temporary mode to the last saved display configuration

</td>
<td>
SDC_APPLY| SDC_USE_DATABASE_CURRENT

</td>
</tr>
<tr>
<td>
Given only the path information, set the display configuration with the source and target information from the database for the paths and ignore the path order

</td>
<td>
SDC_APPLY | SDC_TOPOLOGY_SUPPLIED | SDC_ALLOW_PATH_ORDER_CHANGES

</td>
</tr>
</table>
 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. All sizes in the DEVMODE structure are in terms of physical pixels, and are not related to the calling context.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>
