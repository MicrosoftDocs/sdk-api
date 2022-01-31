---
UID: NE:evr.MFVideoAspectRatioMode
title: MFVideoAspectRatioMode (evr.h)
description: Specifies the aspect-ratio mode.
helpviewer_keywords: ["MFVideoARMode_Mask","MFVideoARMode_NonLinearStretch","MFVideoARMode_None","MFVideoARMode_PreservePicture","MFVideoARMode_PreservePixel","MFVideoAspectRatioMode","MFVideoAspectRatioMode enumeration [Media Foundation]","c0a34cff-f86f-4005-9320-5dadfdde5808","evr/MFVideoARMode_Mask","evr/MFVideoARMode_NonLinearStretch","evr/MFVideoARMode_None","evr/MFVideoARMode_PreservePicture","evr/MFVideoARMode_PreservePixel","evr/MFVideoAspectRatioMode","mf.mfvideoaspectratiomode"]
old-location: mf\mfvideoaspectratiomode.htm
tech.root: mf
ms.assetid: c0a34cff-f86f-4005-9320-5dadfdde5808
ms.date: 12/05/2018
ms.keywords: MFVideoARMode_Mask, MFVideoARMode_NonLinearStretch, MFVideoARMode_None, MFVideoARMode_PreservePicture, MFVideoARMode_PreservePixel, MFVideoAspectRatioMode, MFVideoAspectRatioMode enumeration [Media Foundation], c0a34cff-f86f-4005-9320-5dadfdde5808, evr/MFVideoARMode_Mask, evr/MFVideoARMode_NonLinearStretch, evr/MFVideoARMode_None, evr/MFVideoARMode_PreservePicture, evr/MFVideoARMode_PreservePixel, evr/MFVideoAspectRatioMode, mf.mfvideoaspectratiomode
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
req.typenames: MFVideoAspectRatioMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVideoAspectRatioMode
 - evr/MFVideoAspectRatioMode
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
 - MFVideoAspectRatioMode
---

# MFVideoAspectRatioMode enumeration


## -description

Specifies the aspect-ratio mode.

## -enum-fields

### -field MFVideoARMode_None:0

Do not maintain the aspect ratio of the video. Stretch the video to fit the output rectangle.

### -field MFVideoARMode_PreservePicture:0x1

Preserve the aspect ratio of the video by letterboxing or within the output rectangle.

### -field MFVideoARMode_PreservePixel:0x2

<div class="alert"><b>Note</b>  Currently the EVR ignores this flag.</div>
<div> </div>
Correct the aspect ratio if the physical size of the display device does not match the display resolution. For example, if the native resolution of the monitor is 1600 by 1200 (4:3) but the display resolution is 1280 by 1024 (5:4), the monitor will display non-square pixels.

If this flag is set, you must also set the <b>MFVideoARMode_PreservePicture</b> flag.

### -field MFVideoARMode_NonLinearStretch:0x4

Apply a non-linear horizontal stretch if the aspect ratio of the destination rectangle does not match the aspect ratio of the source rectangle.

The non-linear stretch algorithm preserves the aspect ratio in the middle of the picture and stretches (or shrinks) the image progressively more toward the left and right. This mode is useful when viewing 4:3 content full-screen on a 16:9 display, instead of pillar-boxing. Non-linear vertical stretch is not supported, because the visual results are generally poor.

This mode may cause performance degradation.

If this flag is set, you must also set the <b>MFVideoARMode_PreservePixel</b> and <b>MFVideoARMode_PreservePicture</b> flags.

### -field MFVideoARMode_Mask:0x7

Bitmask to validate flag values. This value is not a valid flag.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getaspectratiomode">IMFVideoDisplayControl::GetAspectRatioMode</a>



<a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode">IMFVideoDisplayControl::SetAspectRatioMode</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
