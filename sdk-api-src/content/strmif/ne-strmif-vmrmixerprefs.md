---
UID: NE:strmif.VMRMixerPrefs
title: VMRMixerPrefs (strmif.h)
description: The VMRMixerPrefs enumeration contains flags that specify decimation, filtering, and color space information that will be used when the video image is created on the DirectDraw surface.
helpviewer_keywords: ["MixerPref_ARAdjustXorY","MixerPref_BiLinearFiltering","MixerPref_DecimateMask","MixerPref_DecimateOutput","MixerPref_DecimationReserved","MixerPref_DynamicDecimateBy2","MixerPref_DynamicMask","MixerPref_DynamicReserved","MixerPref_DynamicSwitchToBOB","MixerPref_FilteringMask","MixerPref_NoDecimation","MixerPref_PointFiltering","MixerPref_RenderTargetMask","MixerPref_RenderTargetRGB","MixerPref_RenderTargetReserved","MixerPref_RenderTargetYUV","MixerPref_RenderTargetYUV420","MixerPref_RenderTargetYUV422","MixerPref_RenderTargetYUV444","VMRMixerPrefs","VMRMixerPrefs enumeration [DirectShow]","VMRMixerPrefsEnumeration","dshow.vmrmixerprefs","strmif/MixerPref_ARAdjustXorY","strmif/MixerPref_BiLinearFiltering","strmif/MixerPref_DecimateMask","strmif/MixerPref_DecimateOutput","strmif/MixerPref_DecimationReserved","strmif/MixerPref_DynamicDecimateBy2","strmif/MixerPref_DynamicMask","strmif/MixerPref_DynamicReserved","strmif/MixerPref_DynamicSwitchToBOB","strmif/MixerPref_FilteringMask","strmif/MixerPref_NoDecimation","strmif/MixerPref_PointFiltering","strmif/MixerPref_RenderTargetMask","strmif/MixerPref_RenderTargetRGB","strmif/MixerPref_RenderTargetReserved","strmif/MixerPref_RenderTargetYUV","strmif/MixerPref_RenderTargetYUV420","strmif/MixerPref_RenderTargetYUV422","strmif/MixerPref_RenderTargetYUV444","strmif/VMRMixerPrefs"]
old-location: dshow\vmrmixerprefs.htm
tech.root: dshow
ms.assetid: 0852590c-6bca-4261-99c0-fff8a012f18e
ms.date: 12/05/2018
ms.keywords: MixerPref_ARAdjustXorY, MixerPref_BiLinearFiltering, MixerPref_DecimateMask, MixerPref_DecimateOutput, MixerPref_DecimationReserved, MixerPref_DynamicDecimateBy2, MixerPref_DynamicMask, MixerPref_DynamicReserved, MixerPref_DynamicSwitchToBOB, MixerPref_FilteringMask, MixerPref_NoDecimation, MixerPref_PointFiltering, MixerPref_RenderTargetMask, MixerPref_RenderTargetRGB, MixerPref_RenderTargetReserved, MixerPref_RenderTargetYUV, MixerPref_RenderTargetYUV420, MixerPref_RenderTargetYUV422, MixerPref_RenderTargetYUV444, VMRMixerPrefs, VMRMixerPrefs enumeration [DirectShow], VMRMixerPrefsEnumeration, dshow.vmrmixerprefs, strmif/MixerPref_ARAdjustXorY, strmif/MixerPref_BiLinearFiltering, strmif/MixerPref_DecimateMask, strmif/MixerPref_DecimateOutput, strmif/MixerPref_DecimationReserved, strmif/MixerPref_DynamicDecimateBy2, strmif/MixerPref_DynamicMask, strmif/MixerPref_DynamicReserved, strmif/MixerPref_DynamicSwitchToBOB, strmif/MixerPref_FilteringMask, strmif/MixerPref_NoDecimation, strmif/MixerPref_PointFiltering, strmif/MixerPref_RenderTargetMask, strmif/MixerPref_RenderTargetRGB, strmif/MixerPref_RenderTargetReserved, strmif/MixerPref_RenderTargetYUV, strmif/MixerPref_RenderTargetYUV420, strmif/MixerPref_RenderTargetYUV422, strmif/MixerPref_RenderTargetYUV444, strmif/VMRMixerPrefs
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: VMRMixerPrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VMRMixerPrefs
 - strmif/VMRMixerPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRMixerPrefs
---

# VMRMixerPrefs enumeration


## -description

The <b>VMRMixerPrefs</b> enumeration contains flags that specify decimation, filtering, and color space information that will be used when the video image is created on the DirectDraw surface.

## -enum-fields

### -field MixerPref_NoDecimation:0x1

No decimation. The video will be rendered onto the surface in its native size.

### -field MixerPref_DecimateOutput:0x2

Decimate output by 2 in the x and y directions.

### -field MixerPref_ARAdjustXorY:0x4

Adjust the horizontal or vertical size of the video streams to match the target aspect ratio. If this flag is not present, the VMR adjusts the horizontal size only. For more information, see <a href="/windows/desktop/DirectShow/aspect-ratio-correction">Aspect Ratio Correction</a>.

### -field MixerPref_DecimationReserved:0x8

Reserved.

### -field MixerPref_DecimateMask:0xf

Bitmask to isolate the flags that control decimation. (This value is not a valid flag.)

### -field MixerPref_BiLinearFiltering:0x10

Use bi-linear filtering. This is the default type of filtering, but not all cards can support it.

### -field MixerPref_PointFiltering:0x20

Use point filtering.

### -field MixerPref_FilteringMask:0xf0

Bitmask to isolate the flags the control filtering. (This value is not a valid flag.)

### -field MixerPref_RenderTargetRGB:0x100

The render target is an RGB surface.

### -field MixerPref_RenderTargetYUV:0x1000

The render target is a YUV surface. Requires Windows XP Service Pack 2. For more information, see <a href="/windows/desktop/DirectShow/yuv-mixing-mode">YUV Mixing Mode</a>.

### -field MixerPref_RenderTargetYUV420:0x200

The render target is a YUV 4:2:0 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MixerPref_RenderTargetYUV422:0x400

The render target is a YUV 4:2:2 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MixerPref_RenderTargetYUV444:0x800

The render target is a YUV 4:4:4 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MixerPref_RenderTargetReserved:0xe000

Reserved.

### -field MixerPref_RenderTargetMask:0xff00

Bitmask to isolate flags that control the render target. (This value is not a valid flag.)

### -field MixerPref_DynamicSwitchToBOB:0x10000

In YUV mixing mode only, this flag switches the VMR to bob deinterlacing. You can add or remove this flag while the filter graph is running; the change will be applied when the VMR mixer composes the next video frame.

### -field MixerPref_DynamicDecimateBy2:0x20000

In YUV mixing mode only, this flag causes the VMR to decimate the image by a factor of 2 horizontally and vertically. You can add or remove this flag while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.

### -field MixerPref_DynamicReserved:0xc0000

Reserved.

### -field MixerPref_DynamicMask:0xf0000

Bitmask to isolate the MixerPref_DynamicSwitchToBOB and MixerPref_DynamicDecimateBy2 flags. (This value is not a valid flag.)

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-getmixingprefs">IVMRMixerControl::GetMixingPrefs</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-setoutputrect">IVMRMixerControl::SetMixingPrefs</a>
