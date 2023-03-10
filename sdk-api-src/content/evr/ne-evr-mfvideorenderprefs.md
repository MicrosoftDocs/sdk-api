---
UID: NE:evr.MFVideoRenderPrefs
title: MFVideoRenderPrefs (evr.h)
description: Contains flags that define how the enhanced video renderer (EVR) displays the video.
helpviewer_keywords: ["MFVideoRenderPrefs","MFVideoRenderPrefs enumeration [Media Foundation]","MFVideoRenderPrefs_AllowBatching","MFVideoRenderPrefs_AllowOutputThrottling","MFVideoRenderPrefs_AllowScaling","MFVideoRenderPrefs_DoNotClipToDevice","MFVideoRenderPrefs_DoNotRenderBorder","MFVideoRenderPrefs_DoNotRepaintOnStop","MFVideoRenderPrefs_ForceBatching","MFVideoRenderPrefs_ForceOutputThrottling","MFVideoRenderPrefs_ForceScaling","MFVideoRenderPrefs_Mask","a56e7e09-23af-4ad3-9846-4102233ed3c4","evr/MFVideoRenderPrefs","evr/MFVideoRenderPrefs_AllowBatching","evr/MFVideoRenderPrefs_AllowOutputThrottling","evr/MFVideoRenderPrefs_AllowScaling","evr/MFVideoRenderPrefs_DoNotClipToDevice","evr/MFVideoRenderPrefs_DoNotRenderBorder","evr/MFVideoRenderPrefs_DoNotRepaintOnStop","evr/MFVideoRenderPrefs_ForceBatching","evr/MFVideoRenderPrefs_ForceOutputThrottling","evr/MFVideoRenderPrefs_ForceScaling","evr/MFVideoRenderPrefs_Mask","mf.mfvideorenderprefs"]
old-location: mf\mfvideorenderprefs.htm
tech.root: mf
ms.assetid: a56e7e09-23af-4ad3-9846-4102233ed3c4
ms.date: 12/05/2018
ms.keywords: MFVideoRenderPrefs, MFVideoRenderPrefs enumeration [Media Foundation], MFVideoRenderPrefs_AllowBatching, MFVideoRenderPrefs_AllowOutputThrottling, MFVideoRenderPrefs_AllowScaling, MFVideoRenderPrefs_DoNotClipToDevice, MFVideoRenderPrefs_DoNotRenderBorder, MFVideoRenderPrefs_DoNotRepaintOnStop, MFVideoRenderPrefs_ForceBatching, MFVideoRenderPrefs_ForceOutputThrottling, MFVideoRenderPrefs_ForceScaling, MFVideoRenderPrefs_Mask, a56e7e09-23af-4ad3-9846-4102233ed3c4, evr/MFVideoRenderPrefs, evr/MFVideoRenderPrefs_AllowBatching, evr/MFVideoRenderPrefs_AllowOutputThrottling, evr/MFVideoRenderPrefs_AllowScaling, evr/MFVideoRenderPrefs_DoNotClipToDevice, evr/MFVideoRenderPrefs_DoNotRenderBorder, evr/MFVideoRenderPrefs_DoNotRepaintOnStop, evr/MFVideoRenderPrefs_ForceBatching, evr/MFVideoRenderPrefs_ForceOutputThrottling, evr/MFVideoRenderPrefs_ForceScaling, evr/MFVideoRenderPrefs_Mask, mf.mfvideorenderprefs
req.header: evr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFVideoRenderPrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVideoRenderPrefs
 - evr/MFVideoRenderPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr.h
api_name:
 - MFVideoRenderPrefs
---

# MFVideoRenderPrefs enumeration


## -description

Contains flags that define how the enhanced video renderer (EVR) displays the video.

## -enum-fields

### -field MFVideoRenderPrefs_DoNotRenderBorder:0x1

If this flag is set, the EVR does not draw the border color. By default, the EVR draws a border on areas of the destination rectangle that have no video. See <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setbordercolor">IMFVideoDisplayControl::SetBorderColor</a>.

### -field MFVideoRenderPrefs_DoNotClipToDevice:0x2

If this flag is set, the EVR does not clip the video when the video window straddles two monitors. By default, if the video window straddles two monitors, the EVR clips the video to the monitor that contains the largest area of video.

### -field MFVideoRenderPrefs_AllowOutputThrottling:0x4

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow the EVR to limit its output to match GPU bandwidth.

### -field MFVideoRenderPrefs_ForceOutputThrottling:0x8

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR
            to limit its output to match GPU bandwidth.

### -field MFVideoRenderPrefs_ForceBatching:0x10

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR to batch Direct3D <b>Present</b> calls. This optimization enables the system to enter to idle states more frequently, which can reduce power consumption.

### -field MFVideoRenderPrefs_AllowBatching:0x20

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow the EVR to batch Direct3D <b>Present</b> calls.

### -field MFVideoRenderPrefs_ForceScaling:0x40

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR to mix the video inside a rectangle that is smaller than the output rectangle. The EVR will then scale the result to the correct output size. The effective resolution will be lower if this setting is applied.

### -field MFVideoRenderPrefs_AllowScaling:0x80

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow
            the EVR to mix the video inside a rectangle that is smaller than the output rectangle.

### -field MFVideoRenderPrefs_DoNotRepaintOnStop:0x100

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Prevent the EVR from repainting the video window after a stop command. By default, the EVR repaints the video window black after a stop command.

### -field MFVideoRenderPrefs_Mask:0x1ff

Bitmask to validate flag values. This value is not a valid flag.

## -remarks

To set these flags, call <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs">IMFVideoDisplayControl::SetRenderingPrefs</a>.

The flags named "MFVideoRenderPrefs_Allow..." cause the EVR to use lower-quality settings only when requested by the quality manager. (For more information, see <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>.) The flags named "MFVideoRenderPrefs_Force..." cause the video mixer to use lower-quality settings regardless of the quality manager.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
