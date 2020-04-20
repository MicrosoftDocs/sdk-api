---
UID: NF:winuser.QueryDisplayConfig
title: QueryDisplayConfig function (winuser.h)
description: The QueryDisplayConfig function retrieves information about all possible display paths for all display devices, or views, in the current setting.helpviewer_keywords: ["CCD_Functions_4fc57ba2-e10b-4d28-bbaf-a5ded2264e59.xml","QueryDisplayConfig","QueryDisplayConfig function [Display Devices]","display.querydisplayconfig","winuser/QueryDisplayConfig"]
old-location: display\querydisplayconfig.htm
tech.root: display
ms.assetid: b1792d7f-f216-4250-a6b6-a11b251a9cec
ms.date: 12/05/2018
ms.keywords: CCD_Functions_4fc57ba2-e10b-4d28-bbaf-a5ded2264e59.xml, QueryDisplayConfig, QueryDisplayConfig function [Display Devices], display.querydisplayconfig, winuser/QueryDisplayConfig
f1_keywords:
- winuser/QueryDisplayConfig
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryDisplayConfig function


## -description


The <b>QueryDisplayConfig</b> function retrieves information about all possible display paths for all display devices, or views, in the current setting.


## -parameters




### -param flags [in]

The type of information to retrieve. The value for the <i>Flags</i> parameter must be one of the following values.





#### QDC_ALL_PATHS

All the possible path combinations of sources to targets.   

<div class="alert"><b>Note</b>  In the case of any temporary modes, the QDC_ALL_PATHS setting means the mode data returned may not be the same as that which is stored in the persistence database.</div>
<div> </div>


#### QDC_ONLY_ACTIVE_PATHS

Currently active paths only.    

<div class="alert"><b>Note</b>  In the case of any temporary modes, the QDC_ONLY_ACTIVE_PATHS setting means the mode data returned may not be the same as that which is stored in the persistence database.</div>
<div> </div>


#### QDC_DATABASE_CURRENT

Active path as defined in the CCD database for the currently connected displays. 


### -param numPathArrayElements [in, out]

Pointer to a variable that contains the number of elements in <i>pPathInfoArray</i>. This parameter cannot be <b>NULL</b>. If <b>QueryDisplayConfig</b> returns ERROR_SUCCESS, <i>pNumPathInfoElements</i> is updated with the number of valid entries in <i>pPathInfoArray</i>.


### -param pathArray [out]

Pointer to a variable that contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a> elements. Each element in <i>pPathInfoArray</i> describes a single path from a source to a target. The source and target mode information indexes are only valid in combination with the <i>pmodeInfoArray</i> tables that are returned for the API at the same time. This parameter cannot be <b>NULL</b>. The <i>pPathInfoArray</i> is always returned in path priority order. For more information about path priority order, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/path-priority-order">Path Priority Order</a>. 


### -param numModeInfoArrayElements [in, out]

Pointer to a variable that specifies the number in element of the mode information table. This parameter cannot be <b>NULL</b>. If <b>QueryDisplayConfig</b> returns ERROR_SUCCESS, <i>pNumModeInfoArrayElements</i> is updated with the number of valid entries in <i>pModeInfoArray</i>. 


### -param modeInfoArray [out]

Pointer to a variable that contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a> elements. This parameter cannot be <b>NULL</b>. 


### -param currentTopologyId [out, optional]

Pointer to a variable that receives the identifier of the currently active topology in the CCD database. For a list of possible values, see the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ne-wingdi-displayconfig_topology_id">DISPLAYCONFIG_TOPOLOGY_ID</a> enumerated type.

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
The system is not running a graphics driver that was written according to the <a href="https://docs.microsoft.com/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide">Windows Display Driver Model (WDDM)</a>. The function is only supported on a system with a WDDM driver running.

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



As the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdisplayconfigbuffersizes">GetDisplayConfigBufferSizes</a> function can only determine the required array size at a particular moment in time, it is possible that between calls to <b>GetDisplayConfigBufferSizes</b> and <b>QueryDisplayConfig</b> the system configuration will change and the provided array sizes will no longer be sufficient to store the new path data. In this situation, <b>QueryDisplayConfig</b> fails with ERROR_INSUFFICIENT_BUFFER, and the caller should call <b>GetDisplayConfigBufferSizes</b> again to get the new array sizes. The caller should then allocate the correct amount of memory. 

<b>QueryDisplayConfig</b> returns paths in the path array that the <i>pPathInfoArray</i> parameter specifies and the source and target modes in the mode array that the <i>pModeInfoArray</i> parameter specifies. <b>QueryDisplayConfig</b> always returns paths in path priority order. If QDC_ALL_PATHS is set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> returns all the inactive paths after the active paths. 

Full path, source mode, and target mode information is available for all active paths. The <b>ModeInfoIdx</b> members in the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structures for the source and target are set up for these active paths. For inactive paths, returned source and target mode information is not available; therefore, the target information in the path structure is set to default values, and the source and target mode indexes are marked as invalid. For database queries, if the current connect monitors have an entry, <b>QueryDisplayConfig</b> returns full path, source mode, and target mode information (same as for active paths). However, if the database does not have a entry, <b>QueryDisplayConfig</b> returns just the path information with the default target details (same as for inactive paths). 

For an example of how source and target mode information relates to path information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/relationship-of-mode-information-to-path-information">Relationship of Mode Information to Path Information</a>.

The caller can use <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> to obtain additional information about the source or target device, for example, the monitor names and monitor preferred mode and source device name.

If a target is currently being force projected, the <b>statusFlags</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure has one of the DISPLAYCONFIG_TARGET_FORCED_XXX flags set. 

If the QDC_DATABASE_CURRENT flag is set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> returns the topology identifier of the active database topology in the variable that the <i>pCurrentTopologyId</i> parameter points to. If the QDC_ALL_PATHS or QDC_ONLY_ACTIVE_PATHS flag is set in the <i>Flags</i> parameter, the <i>pCurrentTopologyId</i> parameter must be set to <b>NULL</b>; otherwise, <b>QueryDisplayConfig</b> returns ERROR_INVALID_PARAMETER.

If a caller calls <b>QueryDisplayConfig</b> with the QDC_DATABASE_CURRENT flag set in the <i>Flags</i> parameter, <b>QueryDisplayConfig</b> initializes the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_2dregion">DISPLAYCONFIG_2DREGION</a> structure that is specified in the <b>totalSize</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> structure to zeros and does not complete DISPLAYCONFIG_2DREGION.

The DEVMODE structure that is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a> Win32 function (described in the Windows SDK documentation) contains information that relates to both the source and target modes. However, the <a href="https://docs.microsoft.com/windows-hardware/drivers/display/ccd-apis">CCD APIs</a> explicitly separate the source and target mode components.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. All sizes in the DEVMODE structure are in terms of physical pixels, and are not related to the calling context.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_mode_info">DISPLAYCONFIG_MODE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ne-wingdi-displayconfig_topology_id">DISPLAYCONFIG_TOPOLOGY_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
 

 

