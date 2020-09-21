---
UID: NS:tvout._VIDEOPARAMETERS
title: VIDEOPARAMETERS (tvout.h)
description: The video miniport driver receives a pointer to a VIDEOPARAMETERS structure in the InputBuffer member of a VIDEO_REQUEST_PACKET when the IOCTL request is IOCTL_VIDEO_HANDLE_VIDEOPARAMETERS.
helpviewer_keywords: ["*LPVIDEOPARAMETERS","*PVIDEOPARAMETERS","LPVIDEOPARAMETERS","LPVIDEOPARAMETERS structure pointer [Display Devices]","PVIDEOPARAMETERS","PVIDEOPARAMETERS structure pointer [Display Devices]","VIDEOPARAMETERS","VIDEOPARAMETERS structure [Display Devices]","Video_Structs_58a5b287-2296-4c62-be8e-33147cfe0167.xml","display.videoparameters","tvout/LPVIDEOPARAMETERS","tvout/PVIDEOPARAMETERS","tvout/VIDEOPARAMETERS"]
old-location: display\videoparameters.htm
tech.root: display
ms.assetid: 1f889c5b-2a9a-468e-8612-a7c5359f92d4
ms.date: 12/05/2018
ms.keywords: '*LPVIDEOPARAMETERS, *PVIDEOPARAMETERS, LPVIDEOPARAMETERS, LPVIDEOPARAMETERS structure pointer [Display Devices], PVIDEOPARAMETERS, PVIDEOPARAMETERS structure pointer [Display Devices], VIDEOPARAMETERS, VIDEOPARAMETERS structure [Display Devices], Video_Structs_58a5b287-2296-4c62-be8e-33147cfe0167.xml, display.videoparameters, tvout/LPVIDEOPARAMETERS, tvout/PVIDEOPARAMETERS, tvout/VIDEOPARAMETERS'
req.header: tvout.h
req.include-header: Tvout.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: VIDEOPARAMETERS, *PVIDEOPARAMETERS, *LPVIDEOPARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VIDEOPARAMETERS
 - tvout/_VIDEOPARAMETERS
 - PVIDEOPARAMETERS
 - tvout/PVIDEOPARAMETERS
 - VIDEOPARAMETERS
 - tvout/VIDEOPARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tvout.h
api_name:
 - VIDEOPARAMETERS
---

# VIDEOPARAMETERS structure


## -description

The video miniport driver receives a pointer to a VIDEOPARAMETERS structure in the <b>InputBuffer</b> member of a <a href="/windows-hardware/drivers/ddi/content/video/ns-video-_video_request_packet">VIDEO_REQUEST_PACKET</a> when the IOCTL request is <a href="/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_handle_videoparameters">IOCTL_VIDEO_HANDLE_VIDEOPARAMETERS</a>. Depending on the <b>dwCommand</b> member of the VIDEOPARAMETERS structure, the miniport driver should get or set the television connector and copy protection capabilities of the device.

## -struct-fields

### -field Guid

Specifies the globally unique identifier (GUID) for this structure {02C62061-1097-11d1-920F-00A024DF156E}. A video miniport driver must verify the GUID at the start of the structure before processing the structure.

### -field dwOffset

Is reserved and should be ignored by the video miniport driver.

### -field dwCommand

Indicates the action to be performed by the driver. This member can be one of the following values:





#### VP_COMMAND_GET

The miniport driver should return all of the device's TV connector capabilities, current TV connector settings, copy protection capabilities, and current copy protection settings by setting the appropriate flags in <b>dwFlags</b> and setting the values of the members that correspond to those set flags.



#### VP_COMMAND_SET

The miniport driver should set the TV connector and copy protection hardware according to the members of this structure that correspond to the flags set in <b>dwFlags</b>.

### -field dwFlags

Indicates which members of this structure contain valid data. When <b>dwCommand</b> is VP_COMMAND_GET, the driver should set the appropriate bits in this member to indicate in which corresponding members it has returned valid data. When <b>dwCommand</b> is VP_COMMAND_SET, the driver should set the functionality on the hardware according to values in the members that correspond with the bits set in this member. This member can be a bitwise OR of the values listed in the first column of the following table.

<table>
<tr>
<th>Flag</th>
<th>Corresponding Members</th>
<th>Commands</th>
</tr>
<tr>
<td>
VP_FLAGS_BRIGHTNESS

</td>
<td>
<b>dwBrightness</b>

</td>
<td>
get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_CONTRAST

</td>
<td>
<b>dwContrast</b>

</td>
<td>
get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_COPYPROTECT

</td>
<td>
<b>dwCPType</b>

<b>dwCPCommand</b>

<b>dwCPStandard</b>

<b>dwCPKey</b>

<b>bCP_APSTriggerBits</b>

<b>bOEMCopyProtection</b>

</td>
<td>
get/set

set

get

set

set

get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_FLICKER

</td>
<td>
<b>dwFlickerFilter</b>

</td>
<td>
get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_MAX_UNSCALED

</td>
<td>
<b>dwMaxUnscaledX</b>

<b>dwMaxUnscaledY</b>

</td>
<td>
get

get

</td>
</tr>
<tr>
<td>
VP_FLAGS_OVERSCAN

</td>
<td>
<b>dwOverscanX</b>

<b>dwOverscanY</b>

</td>
<td>
get/set

get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_POSITION

</td>
<td>
<b>dwPositionX</b>

<b>dwPositionY</b>

</td>
<td>
get/set

get/set

</td>
</tr>
<tr>
<td>
VP_FLAGS_TV_MODE

</td>
<td>
<b>dwMode</b>

<b>dwAvailableModes</b>

</td>
<td>
get/set

get

</td>
</tr>
<tr>
<td>
VP_FLAGS_TV_STANDARD

</td>
<td>
<b>dwTVStandard</b>

<b>dwAvailableTVStandard</b>

</td>
<td>
get/set

get

</td>
</tr>
</table>

### -field dwMode

Specifies the current playback mode. This member is valid for both the VP_COMMAND_SET and VP_COMMAND_GET commands, and can be one of the following values:





#### VP_MODE_TV_PLAYBACK

Describes an optimal set of fields for video playback, with the flicker filter off and overscan display on.



#### VP_MODE_WIN_GRAPHICS

Describes the display settings that are optimal for Windows display, with the maximum flicker filter on and any overscan display off.

### -field dwTVStandard

Is the current world television standard. This member is valid for both the VP_COMMAND_SET and VP_COMMAND_GET commands, and can be one of the following values:

VP_TV_STANDARD_NTSC_M

VP_TV_STANDARD_NTSC_M_J

VP_TV_STANDARD_NTSC_433

VP_TV_STANDARD_PAL_B

VP_TV_STANDARD_PAL_D

VP_TV_STANDARD_PAL_G

VP_TV_STANDARD_PAL_H

VP_TV_STANDARD_PAL_I

VP_TV_STANDARD_PAL_M

VP_TV_STANDARD_PAL_N

VP_TV_STANDARD_PAL_60

VP_TV_STANDARD_SECAM_B

VP_TV_STANDARD_SECAM_D

VP_TV_STANDARD_SECAM_G

VP_TV_STANDARD_SECAM_H

VP_TV_STANDARD_SECAM_K

VP_TV_STANDARD_SECAM_K1

VP_TV_STANDARD_SECAM_L

VP_TV_STANDARD_SECAM_L1

VP_TV_STANDARD_WIN_VGA

### -field dwAvailableModes

Indicates the playback modes the device is capable of. This member is only valid for the VP_COMMAND_GET command, and can be a bitwise OR of the following values:

VP_MODE_TV_PLAYBACK

VP_MODE_WIN_GRAPHICS

### -field dwAvailableTVStandard

Specifies all available world television standards. This member is only valid for the VP_COMMAND_GET command, and can be a bitwise OR of the following values:

VP_TV_STANDARD_NTSC_M

VP_TV_STANDARD_NTSC_M_J

VP_TV_STANDARD_NTSC_433

VP_TV_STANDARD_PAL_B

VP_TV_STANDARD_PAL_D

VP_TV_STANDARD_PAL_G

VP_TV_STANDARD_PAL_H

VP_TV_STANDARD_PAL_I

VP_TV_STANDARD_PAL_M

VP_TV_STANDARD_PAL_N

VP_TV_STANDARD_PAL_60

VP_TV_STANDARD_SECAM_B

VP_TV_STANDARD_SECAM_D

VP_TV_STANDARD_SECAM_G

VP_TV_STANDARD_SECAM_H

VP_TV_STANDARD_SECAM_K

VP_TV_STANDARD_SECAM_K1

VP_TV_STANDARD_SECAM_L

VP_TV_STANDARD_SECAM_L1

VP_TV_STANDARD_WIN_VGA

### -field dwFlickerFilter

Is a value in tenths of a percent that indicates the flicker filter state. This member can be a value between [0,1000], and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwOverScanX

Is a value in tenths of a percent that indicates the amount of overscan in <i>x</i>. This member can be a value between [0,1000], and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwOverScanY

Is a value in tenths of a percent that indicates the amount of overscan in <i>y</i>. This member can be a value between [0,1000], and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwMaxUnscaledX

Is the maximum <i>x</i> resolution that the TV can display without having the hardware scale the video image. The miniport driver must set a value in this member when <b>dwCommand</b> is VP_COMMAND_GET. This member is invalid for VP_COMMAND_SET.

### -field dwMaxUnscaledY

Is the maximum <i>y</i> resolution that the TV can display without having the hardware scale the video image. The miniport driver must set a value in this member when <b>dwCommand</b> is VP_COMMAND_GET. This member is invalid for VP_COMMAND_SET.

### -field dwPositionX

Is the value used by the hardware to determine the current <i>x</i> position of the image on the TV. This member is specified in pixels, and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwPositionY

Is the value used by the hardware to determine the current <i>y</i> position of the image on the TV. This member is specified in scan lines, and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwBrightness

Is a percentage value that indicates the brightness setting on the TV. This member can be a value between [0,100], and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwContrast

Is a percentage value that indicates the contrast setting on the TV. This member can be a value between [0,100], and is valid for both VP_COMMAND_GET and VP_COMMAND_SET.

### -field dwCPType

Specifies the type of copy protection supported by the device. This member is valid for both the VP_COMMAND_SET and VP_COMMAND_GET commands, and can be CP_TYPE_APS_TRIGGER.

### -field dwCPCommand

Is the copy protection command. This member is only valid for the VP_COMMAND_SET command, and can be one of the following values:





#### VP_CP_CMD_ACTIVATE

The miniport driver should turn on copy protection and generate and return a unique copy protection key in <b>dwCPKey</b>.



#### VP_CP_CMD_CHANGE

If the copy protection key in <b>dwCPKey</b> is valid, the miniport driver should change copy protection based on the trigger data in <b>bCP_APSTriggerBits</b>.



#### VP_CP_CMD_DEACTIVATE

If the copy protection key in <b>dwCPKey</b> is valid, the miniport driver should turn off copy protection.

### -field dwCPStandard

Is the TV standards for which copy protection types are available. This member is only valid for the VP_COMMAND_GET command, and can be a bitwise OR of the following values:

VP_TV_STANDARD_NTSC_M

VP_TV_STANDARD_NTSC_M_J

VP_TV_STANDARD_NTSC_433

VP_TV_STANDARD_PAL_B

VP_TV_STANDARD_PAL_D

VP_TV_STANDARD_PAL_G

VP_TV_STANDARD_PAL_H

VP_TV_STANDARD_PAL_I

VP_TV_STANDARD_PAL_M

VP_TV_STANDARD_PAL_N

VP_TV_STANDARD_PAL_60

VP_TV_STANDARD_SECAM_B

VP_TV_STANDARD_SECAM_D

VP_TV_STANDARD_SECAM_G

VP_TV_STANDARD_SECAM_H

VP_TV_STANDARD_SECAM_K

VP_TV_STANDARD_SECAM_K1

VP_TV_STANDARD_SECAM_L

VP_TV_STANDARD_SECAM_L1

VP_TV_STANDARD_WIN_VGA

### -field dwCPKey

Is a driver-generated copy protection key that is unique to this instance of the driver. This member is valid only for the VP_COMMAND_SET command. The miniport driver generates and returns this key when <b>dwCPCommand</b> is set to VP_CP_CMD_ACTIVATE. The caller must set this key when the <b>dwCPCommand</b> field is either VP_CP_CMD_DEACTIVATE or VP_CP_CMD_CHANGE. If the caller sets an incorrect key, the driver must not change the current copy protection settings.

### -field bCP_APSTriggerBits

Specifies DVD analog protection system (APS) trigger bit data. Bits zero and 1 are valid. This member is valid only for the VP_COMMAND_SET command.

### -field bOEMCopyProtection

OEM-specific copy protection data. This member is valid for both the VP_COMMAND_SET and VP_COMMAND_GET commands.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ntddvdeo/ni-ntddvdeo-ioctl_video_handle_videoparameters">IOCTL_VIDEO_HANDLE_VIDEOPARAMETERS</a>



<a href="/windows-hardware/drivers/ddi/content/video/ns-video-_video_request_packet">VIDEO_REQUEST_PACKET</a>