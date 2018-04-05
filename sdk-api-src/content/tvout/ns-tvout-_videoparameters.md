---
UID: NS:tvout._VIDEOPARAMETERS
title: "_VIDEOPARAMETERS"
author: windows-driver-content
description: The VIDEOPARAMETERS structure contains information for a video connection.
old-location: gdi\videoparameters.htm
old-project: gdi
ms.assetid: ca5368ac-adf6-4f1d-abfd-4615dd0c6a68
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPVIDEOPARAMETERS, *PVIDEOPARAMETERS, PVIDEOPARAMETERS, PVIDEOPARAMETERS structure pointer [Windows GDI], VIDEOPARAMETERS, VIDEOPARAMETERS structure [Windows GDI], VIDOEPARAMETERS, VIDOEPARAMETERS structure [Windows GDI], _VIDEOPARAMETERS, _win32_VIDEOPARAMETERS_str, gdi.videoparameters, tvout/PVIDEOPARAMETERS, tvout/VIDEOPARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tvout.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIDEOPARAMETERS, *PVIDEOPARAMETERS, *LPVIDEOPARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tvout.h
api_name:
-	VIDOEPARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _VIDEOPARAMETERS structure


## -description



The <b>VIDEOPARAMETERS</b> structure contains information for a video connection.




## -struct-fields




### -field Guid

 


### -field dwOffset

Reserved; must be zero.


### -field dwCommand

Specifies whether to retrieve or set the values that are indicated by the other members of this structure. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>VP_COMMAND_GET</td>
<td>Gets current video capabilities. If capability is not supported, <b>dwFlags</b> is 0.</td>
</tr>
<tr>
<td>VP_COMMAND_SET</td>
<td>Sets video parameters.</td>
</tr>
</table>
 


### -field dwFlags

Indicates which fields contain valid data. For VP_COMMAND_GET, this should be zero. For VP_COMMAND_SET, these are the fields to set. It can be any combination of the following.

<table>
<tr>
<th>Value</th>
<th>Fields containing data</th>
</tr>
<tr>
<td>VP_FLAGS_TV_MODE</td>
<td><b>dwMode</b> (for VP_COMMAND_GET and VP_COMMAND_SET) and <b>dwAvailableModes</b> (for VP_COMMAND_GET).</td>
</tr>
<tr>
<td>VP_FLAGS_TV_STANDARD</td>
<td><b>dwTVStandard</b> (for VP_COMMAND_GET and VP_COMMAND_SET) and <b>dwAvailableTVStandard</b> (for VP_COMMAND_GET).</td>
</tr>
<tr>
<td>VP_FLAGS_FLICKER</td>
<td><b>dwFlickerFilter</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
<tr>
<td>VP_FLAGS_OVERSCAN</td>
<td><b>dwOverScanX</b>, <b>dwOverScanY</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
<tr>
<td>VP_FLAGS_MAX_UNSCALED</td>
<td><b>dwMaxUnscaledX</b>, <b>dwMaxUnscaledY</b> (for VP_COMMAND_GET).</td>
</tr>
<tr>
<td>VP_FLAGS_POSITION</td>
<td><b>dwPositionX</b>, <b>dwPositionY</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
<tr>
<td>VP_FLAGS_BRIGHTNESS</td>
<td><b>dwBrightness</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
<tr>
<td>VP_FLAGS_CONTRAST</td>
<td><b>dwContrast</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
<tr>
<td>VP_FLAGS_COPYPROTECT</td>
<td><b>dwCPType</b> (for VP_COMMAND_GET and VP_COMMAND_SET), <b>dwCPCommand</b> (for VP_COMMAND_SET), <b>dwCPStandard</b> (for VP_COMMAND_GET), <b>dwCPKey</b> (for VP_COMMAND_SET), <b>bCP_APSTriggerBits</b>, <b>bOEMCopyProtection</b> (for VP_COMMAND_GET and VP_COMMAND_SET).</td>
</tr>
</table>
 


### -field dwMode

The current playback mode. This member is valid for both VP_COMMAND_GET and VP_COMMAND_SET. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>VP_MODE_WIN_GRAPHICS</td>
<td>Describes a set of display settings that are optimal for Windows display, with the flicker filter on and any overscan display off.</td>
</tr>
<tr>
<td>VP_MODE_TV_PLAYBACK</td>
<td>Describes a set of display settings for video playback, with the flicker filter off and the overscan display on.</td>
</tr>
</table>
 


### -field dwTVStandard

The TV standard. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET. It can be any one of the following.

<ul>
<li>VP_TV_STANDARD_NTSC_433</li>
<li>VP_TV_STANDARD_NTSC_M</li>
<li>VP_TV_STANDARD_NTSC_M_J</li>
<li>VP_TV_STANDARD_PAL_60</li>
<li>VP_TV_STANDARD_PAL_B</li>
<li>VP_TV_STANDARD_PAL_D</li>
<li>VP_TV_STANDARD_PAL_G</li>
<li>VP_TV_STANDARD_PAL_H</li>
<li>VP_TV_STANDARD_PAL_I</li>
<li>VP_TV_STANDARD_PAL_M</li>
<li>VP_TV_STANDARD_PAL_N</li>
<li>VP_TV_STANDARD_SECAM_B</li>
<li>VP_TV_STANDARD_SECAM_D</li>
<li>VP_TV_STANDARD_SECAM_G</li>
<li>VP_TV_STANDARD_SECAM_H</li>
<li>VP_TV_STANDARD_SECAM_K</li>
<li>VP_TV_STANDARD_SECAM_K1</li>
<li>VP_TV_STANDARD_SECAM_L</li>
<li>VP_TV_STANDARD_SECAM_L1</li>
<li>VP_TV_STANDARD_WIN_VGA</li>
</ul>

### -field dwAvailableModes

Specifies which modes are available. This is valid only for VP_COMMAND_GET. It can be any combination of the values specified in <b>dwMode</b>.


### -field dwAvailableTVStandard

The TV standards that are available. This is valid only for VP_COMMAND_GET. It can be any combination of the values specified in <b>dwTVStandard</b>.


### -field dwFlickerFilter

The flicker reduction provided by the hardware. This is a percentage value in tenths of a percent, from 0 to 1,000, where 0 is no flicker reduction and 1,000 is maximum flicker reduction. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwOverScanX

The amount of overscan in the horizontal direction. This is a percentage value in tenths of a percent, from 0 to 1,000. A value of 0 indicates no overscan, ensuring that the entire display is visible. A value of 1,000 is maximum overscan and typically causes some of the image to be off the edge of the screen. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwOverScanY

The amount of overscan in the vertical direction. This is a percentage value in tenths of a percent, from 0 to 1,000. A value of 0 indicates no overscan, ensuring that the entire display is visible. A value of 1,000 is maximum overscan and typically causes some of the image to be off the edge of the screen. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwMaxUnscaledX

The maximum horizontal resolution, in pixels, that is supported when the video is not scaled. This field is valid for both VP_COMMAND_GET.


### -field dwMaxUnscaledY

The maximum vertical resolution, in pixels, that is supported when the video is not scaled. This field is valid for both VP_COMMAND_GET.


### -field dwPositionX

The horizontal adjustment to the center of the image. Units are in pixels. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwPositionY

The vertical adjustment to the center of the image. Units are in scan lines. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwBrightness

Adjustment to the DC offset of the video signal to increase brightness on the television. It is a percentage value, 0 to 100, where 0 means no adjustment and 100 means maximum adjustment. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwContrast

Adjustment to the gain of the video signal to increase the intensity of whiteness on the television. It is a percentage value, 0 to 100, where 0 means no adjustment and 100 means maximum adjustment. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


### -field dwCPType

The copy protection type. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>VP_CP_TYPE_APS_TRIGGER</td>
<td>Only DVD trigger bits available.</td>
</tr>
<tr>
<td>VP_CP_TYPE_MACROVISION</td>
<td>Full Macrovision data is available.</td>
</tr>
</table>
 


### -field dwCPCommand

The copy protection command. This field is only valid for VP_COMMAND_SET. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>VP_CP_CMD_ACTIVATE</td>
<td>Activate copy protection.</td>
</tr>
<tr>
<td>VP_CP_CMD_CHANGE</td>
<td>Change copy protection.</td>
</tr>
<tr>
<td>VP_CP_CMD_DEACTIVATE</td>
<td>Deactivate copy protection.</td>
</tr>
</table>
 


### -field dwCPStandard

Specifies TV standards for which copy protection types are available. This field is valid only for VP_COMMAND_GET.


### -field dwCPKey

The copy protection key returned if <b>dwCPCommand</b> is set to VP_CP_CMD_ACTIVATE. The caller must set this key when the <b>dwCPCommand</b> field is either VP_CP_CMD_DEACTIVATE or VP_CP_CMD_CHANGE. If the caller sets an incorrect key, the driver must not change the current copy protection settings. This field is valid only for VP_COMMAND_SET.


### -field bCP_APSTriggerBits

The DVD APS trigger bit flag. This is valid only for VP_COMMAND_SET. Currently, only bits 0 and 1 are valid. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>No copy protection.</td>
</tr>
<tr>
<td>1, 2, or 3</td>
<td>Macrovision-defined analog protection methods.</td>
</tr>
</table>
 


### -field bOEMCopyProtection

The OEM-specific copy protection data. Maximum of 256 characters. This field is valid for both VP_COMMAND_GET and VP_COMMAND_SET.


#### - guid

The GUID for this structure. {02C62061-1097-11d1-920F-00A024DF156E}. Display drivers should verify the GUID at the start of the structure before processing the structure.


## -see-also




<a href="https://msdn.microsoft.com/1448e04c-1452-4eab-bda4-4d249cb67a24">
        ChangeDisplaySettingsEx
      </a>



<a href="https://msdn.microsoft.com/0a1023ee-0cab-4978-ad4c-57637379def9">Device Context Structures</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>
 

 

