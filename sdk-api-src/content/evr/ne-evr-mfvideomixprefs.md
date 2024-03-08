---
UID: NE:evr._MFVideoMixPrefs
title: MFVideoMixPrefs (evr.h)
description: Contains flags that are used to configure how the enhanced video renderer (EVR) performs deinterlacing.
helpviewer_keywords: ["MFVideoMixPrefs","MFVideoMixPrefs enumeration [Media Foundation]","MFVideoMixPrefs_AllowDropToBob","MFVideoMixPrefs_AllowDropToHalfInterlace","MFVideoMixPrefs_ForceBob","MFVideoMixPrefs_ForceHalfInterlace","MFVideoMixPrefs_Mask","evr/MFVideoMixPrefs","evr/MFVideoMixPrefs_AllowDropToBob","evr/MFVideoMixPrefs_AllowDropToHalfInterlace","evr/MFVideoMixPrefs_ForceBob","evr/MFVideoMixPrefs_ForceHalfInterlace","evr/MFVideoMixPrefs_Mask","mf.mfvideomixprefs"]
old-location: mf\mfvideomixprefs.htm
tech.root: mfarchive
ms.assetid: 28dcc8b1-684e-4178-9606-118e77d8ff58
ms.date: 12/05/2018
ms.keywords: MFVideoMixPrefs, MFVideoMixPrefs enumeration [Media Foundation], MFVideoMixPrefs_AllowDropToBob, MFVideoMixPrefs_AllowDropToHalfInterlace, MFVideoMixPrefs_ForceBob, MFVideoMixPrefs_ForceHalfInterlace, MFVideoMixPrefs_Mask, evr/MFVideoMixPrefs, evr/MFVideoMixPrefs_AllowDropToBob, evr/MFVideoMixPrefs_AllowDropToHalfInterlace, evr/MFVideoMixPrefs_ForceBob, evr/MFVideoMixPrefs_ForceHalfInterlace, evr/MFVideoMixPrefs_Mask, mf.mfvideomixprefs
req.header: evr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFVideoMixPrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoMixPrefs
 - evr/_MFVideoMixPrefs
 - MFVideoMixPrefs
 - evr/MFVideoMixPrefs
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
 - MFVideoMixPrefs
archived: true
---

# MFVideoMixPrefs enumeration


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Contains flags that are used to configure how the enhanced video renderer (EVR) performs  deinterlacing.

## -enum-fields

### -field MFVideoMixPrefs_ForceHalfInterlace:0x1

Force the EVR  to skip the second field (in temporal order) of every interlaced frame.

### -field MFVideoMixPrefs_AllowDropToHalfInterlace:0x2

If the EVR is falling behind, allow it to skip the second field (in temporal order) of every interlaced frame.

### -field MFVideoMixPrefs_AllowDropToBob:0x4

If the EVR is falling behind, allow it to use bob deinterlacing, even if the driver supports a higher-quality deinterlacing mode.

### -field MFVideoMixPrefs_ForceBob:0x8

Force the EVR to use bob deinterlacing, even if the driver supports a higher-quality mode.

### -field MFVideoMixPrefs_EnableRotation:0x10

### -field MFVideoMixPrefs_Mask:0x1f

The bitmask of valid flag values. This constant is not itself a valid flag.

## -remarks

To set these flags, call the <a href="/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs">IMFVideoMixerControl2::SetMixingPrefs</a> method.

These flags control some trade-offs between video quality and rendering speed. The constants named "MFVideoMixPrefs_Allow..." enable lower-quality settings, but only when the quality manager requests a drop in quality.  The constants named "MFVideoMixPrefs_Force..." force the EVR to use lower-quality settings regardless of  what the quality manager requests. (For more information about the quality manager, see <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>.)

Currently two lower-quality modes are supported, as described in the following table. Either is preferable to dropping an entire frame.



<table>
<tr>
<th>Mode</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="Half_interface"></a><a id="half_interface"></a><a id="HALF_INTERFACE"></a>Half interface

</td>
<td width="60%">
The EVR's video mixer skips the second field (relative to temporal order) of each interlaced frame. The video mixer still deinterlaces the first field, and this operation typically interpolates data from the second field. The overall frame rate is unaffected.

</td>
</tr>
<tr>
<td width="40%">
<a id="Bob_deinterlacing"></a><a id="bob_deinterlacing"></a><a id="BOB_DEINTERLACING"></a>Bob deinterlacing

</td>
<td width="60%">
The video mixer uses bob deinterlacing, even if the driver supports  a higher-quality deinterlacing algorithm.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
