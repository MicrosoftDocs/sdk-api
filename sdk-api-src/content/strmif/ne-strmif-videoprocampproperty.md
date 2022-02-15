---
UID: NE:strmif.tagVideoProcAmpProperty
title: VideoProcAmpProperty (strmif.h)
description: The VideoProcAmpProperty enumeration specifies video properties on a video capture device.
helpviewer_keywords: ["VideoProcAmpProperty","VideoProcAmpProperty enumeration [DirectShow]","VideoProcAmpPropertyEnumeration","VideoProcAmp_BacklightCompensation","VideoProcAmp_Brightness","VideoProcAmp_ColorEnable","VideoProcAmp_Contrast","VideoProcAmp_Gain","VideoProcAmp_Gamma","VideoProcAmp_Hue","VideoProcAmp_Saturation","VideoProcAmp_Sharpness","VideoProcAmp_WhiteBalance","dshow.videoprocampproperty","strmif/VideoProcAmpProperty","strmif/VideoProcAmp_BacklightCompensation","strmif/VideoProcAmp_Brightness","strmif/VideoProcAmp_ColorEnable","strmif/VideoProcAmp_Contrast","strmif/VideoProcAmp_Gain","strmif/VideoProcAmp_Gamma","strmif/VideoProcAmp_Hue","strmif/VideoProcAmp_Saturation","strmif/VideoProcAmp_Sharpness","strmif/VideoProcAmp_WhiteBalance"]
old-location: dshow\videoprocampproperty.htm
tech.root: dshow
ms.assetid: 113e3896-4920-41a3-9ce2-a26c34af4896
ms.date: 12/05/2018
ms.keywords: VideoProcAmpProperty, VideoProcAmpProperty enumeration [DirectShow], VideoProcAmpPropertyEnumeration, VideoProcAmp_BacklightCompensation, VideoProcAmp_Brightness, VideoProcAmp_ColorEnable, VideoProcAmp_Contrast, VideoProcAmp_Gain, VideoProcAmp_Gamma, VideoProcAmp_Hue, VideoProcAmp_Saturation, VideoProcAmp_Sharpness, VideoProcAmp_WhiteBalance, dshow.videoprocampproperty, strmif/VideoProcAmpProperty, strmif/VideoProcAmp_BacklightCompensation, strmif/VideoProcAmp_Brightness, strmif/VideoProcAmp_ColorEnable, strmif/VideoProcAmp_Contrast, strmif/VideoProcAmp_Gain, strmif/VideoProcAmp_Gamma, strmif/VideoProcAmp_Hue, strmif/VideoProcAmp_Saturation, strmif/VideoProcAmp_Sharpness, strmif/VideoProcAmp_WhiteBalance
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
req.typenames: VideoProcAmpProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVideoProcAmpProperty
 - strmif/tagVideoProcAmpProperty
 - VideoProcAmpProperty
 - strmif/VideoProcAmpProperty
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
 - VideoProcAmpProperty
---

# VideoProcAmpProperty enumeration


## -description

The <b>VideoProcAmpProperty</b> enumeration specifies video properties on a video capture device.

## -enum-fields

### -field VideoProcAmp_Brightness:0

Specifies the brightness, also called the <i>black level</i>. For NTSC, the value is expressed in IRE units * 100. For non-NTSC sources, the units are arbitrary, with zero representing blanking and 10,000 representing pure white. Values range from –10,000 to 10,000.

### -field VideoProcAmp_Contrast

Specifies the contrast, expressed as gain factor * 100. Values range from zero to 10,000.

### -field VideoProcAmp_Hue

Specifies the hue, in degrees * 100. Values range from -180,000 to 180,000 (-180 to +180 degrees).

### -field VideoProcAmp_Saturation

Specifies the saturation. Values range from 0 to 10,000.

### -field VideoProcAmp_Sharpness

Specifies the sharpness. Values range from 0 to 100.

### -field VideoProcAmp_Gamma

Specifies the gamma, as gamma * 100. Values range from 1 to 500.

### -field VideoProcAmp_ColorEnable

Specifies the color enable setting. The possible values are 0 (off) and 1 (on).

### -field VideoProcAmp_WhiteBalance

Specifies the white balance, as a color temperature in degrees Kelvin. The range of values depends on the device.

### -field VideoProcAmp_BacklightCompensation

Specifies the backlight compensation setting. Possible values are 0 (off) and 1 (on).

### -field VideoProcAmp_Gain

Specifies the gain adjustment. Zero is normal. Positive values are brighter and negative values are darker. The range of values depends on the device.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp</a>
