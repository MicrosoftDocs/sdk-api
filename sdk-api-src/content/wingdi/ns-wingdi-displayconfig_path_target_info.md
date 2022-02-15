---
UID: NS:wingdi.DISPLAYCONFIG_PATH_TARGET_INFO
title: DISPLAYCONFIG_PATH_TARGET_INFO (wingdi.h)
description: The DISPLAYCONFIG_PATH_TARGET_INFO structure contains target information for a single path.
helpviewer_keywords: ["CCD_Structures_b33adc91-e83f-42dc-a56a-536bf99cdb7f.xml","DISPLAYCONFIG_PATH_TARGET_INFO","DISPLAYCONFIG_PATH_TARGET_INFO structure [Display Devices]","display.displayconfig_path_target_info","wingdi/DISPLAYCONFIG_PATH_TARGET_INFO"]
old-location: display\displayconfig_path_target_info.htm
tech.root: display
ms.assetid: 3dcdca96-7c5d-4e69-b7dd-8b5ccda25f6a
ms.date: 12/05/2018
ms.keywords: CCD_Structures_b33adc91-e83f-42dc-a56a-536bf99cdb7f.xml, DISPLAYCONFIG_PATH_TARGET_INFO, DISPLAYCONFIG_PATH_TARGET_INFO structure [Display Devices], display.displayconfig_path_target_info, wingdi/DISPLAYCONFIG_PATH_TARGET_INFO
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DISPLAYCONFIG_PATH_TARGET_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_PATH_TARGET_INFO
 - wingdi/DISPLAYCONFIG_PATH_TARGET_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_PATH_TARGET_INFO
---

# DISPLAYCONFIG_PATH_TARGET_INFO structure


## -description

The DISPLAYCONFIG_PATH_TARGET_INFO structure contains target information for a single path.

## -struct-fields

### -field adapterId

The identifier of the adapter that the path is on.

### -field id

The target identifier on the specified adapter that this path relates to.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.modeInfoIdx

A valid index into the mode information table that contains the target mode information for this path only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is not set. If target mode information is not available, the value of <b>modeInfoIdx</b> is DISPLAYCONFIG_PATH_MODE_IDX_INVALID.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.desktopModeInfoIdx

A valid index into the mode array of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_desktop_image_info">DISPLAYCONFIG_DESKTOP_IMAGE_INFO</a> entry that contains the desktop mode information for this path only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is set. If there is no entry for this in the mode array, the value of <b>desktopModeInfoIdx</b> is DISPLAYCONFIG_PATH_DESKTOP_IMAGE_IDX_INVALID. Supported starting in Windows 10.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.targetModeInfoIdx

A valid index into the mode array of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a> entry that contains the target mode information for this path only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is set. If there is no entry for this in the mode array, the value of <b>targetModeInfoIdx</b> is DISPLAYCONFIG_PATH_TARGET_MODE_IDX_INVALID. Supported starting in Windows 10.

### -field outputTechnology

The target's connector type. For a list of possible values, see the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a> enumerated type.

### -field rotation

A value that specifies the rotation of the target. For a list of possible values, see the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_rotation">DISPLAYCONFIG_ROTATION</a> enumerated type.

### -field scaling

A value that specifies how the source image is scaled to the target. For a list of possible values, see the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_scaling">DISPLAYCONFIG_SCALING</a> enumerated type. For more information about scaling, see <a href="/windows-hardware/drivers/display/scaling-the-desktop-image">Scaling the Desktop Image</a>.

### -field refreshRate

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_rational">DISPLAYCONFIG_RATIONAL</a> structure that specifies the refresh rate of the target. If the caller specifies target mode information, the operating system will instead use the refresh rate that is stored in the <b>vSyncFreq</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> structure. In this case, the caller specifies this value in the <b>targetVideoSignalInfo</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a> structure. A refresh rate with both the numerator and denominator set to zero indicates that the caller does not specify a refresh rate and the operating system should use the most optimal refresh rate available. For this case, in a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> function, the caller must set the <b>scanLineOrdering</b> member to the DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED value; otherwise, <b>SetDisplayConfig</b> fails.

### -field scanLineOrdering

A value that specifies the scan-line ordering of the output on the target. For a list of possible values, see the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_scanline_ordering">DISPLAYCONFIG_SCANLINE_ORDERING</a> enumerated type. If the caller specifies target mode information, the operating system will instead use the scan-line ordering that is stored in the <b>scanLineOrdering</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> structure. In this case, the caller specifies this value in the <b>targetVideoSignalInfo</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a> structure.

### -field targetAvailable

A Boolean value that specifies whether the target is available. <b>TRUE</b> indicates that the target is available.

Because the asynchronous nature of display topology changes when a monitor is removed, a path might still be marked as active even though the monitor has been removed. In such a case, <b>targetAvailable</b> could be <b>FALSE</b> for an active path. This is typically a transient situation that will change after the operating system  takes action on the monitor removal.

### -field statusFlags

A bitwise OR of flag values that indicates the status of the target. The following values are supported:


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_IN_USE"></a><a id="displayconfig_target_in_use"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_IN_USE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Target is in use on an active path.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_FORCIBLE"></a><a id="displayconfig_target_forcible"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_FORCIBLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The output can be forced on this target even if a monitor is not detected.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_BOOT"></a><a id="displayconfig_target_forced_availability_boot"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_BOOT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Output is currently being forced in a boot-persistent manner.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_PATH"></a><a id="displayconfig_target_forced_availability_path"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_PATH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Output is currently being forced in a path-persistent manner.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_SYSTEM"></a><a id="displayconfig_target_forced_availability_system"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_FORCED_AVAILABILITY_SYSTEM</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Output is currently being forced in a nonpersistent manner.
</td>
</tr>
<tr>
<td width="40%"><a id="DISPLAYCONFIG_TARGET_IS_HMD"></a><a id="displayconfig_target_is_hmd"></a><dl>
<dt><b>DISPLAYCONFIG_TARGET_IS_HMD</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The output is a head-mounted display (HMD). Such a path is only returned from QueryDisplayConfig using the QDC_INCLUDE_HMD flag.

Supported starting in the Windows 10 Creators Update (Version 1703).
</td>
</tr>
</table>

## -remarks

A DISPLAYCONFIG_PATH_TARGET_INFO structure is specified in the <b>targetInfo</b> member of a <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a> structure.

A target corresponds to the number of possible video outputs on a display adapter. This number, however, does not equate to the number of physical connectors on the display adapter. Each connector exposes a number of targets that includes backward compatibility with older connector technology. For example, a DVI connector exposes a DVI target, as well as a VGA target. A DisplayPort connector, which was introduced in 2006, exposes DisplayPort, HDMI, DVI, legacy TV, and VGA targets.

The <b>statusFlags</b> member is set when you call the <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_info">DISPLAYCONFIG_PATH_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_rational">DISPLAYCONFIG_RATIONAL</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_rotation">DISPLAYCONFIG_ROTATION</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_scaling">DISPLAYCONFIG_SCALING</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_scanline_ordering">DISPLAYCONFIG_SCANLINE_ORDERING</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>