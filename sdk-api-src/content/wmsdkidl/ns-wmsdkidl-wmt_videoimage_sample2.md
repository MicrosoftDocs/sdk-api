---
UID: NS:wmsdkidl.__WMT_VIDEOIMAGE_SAMPLE2
title: WMT_VIDEOIMAGE_SAMPLE2 (wmsdkidl.h)
description: The WMT_VIDEOIMAGE_SAMPLE2 structure describes a sample for a Video Image stream.
helpviewer_keywords: ["WMT_VIDEOIMAGE_SAMPLE2","WMT_VIDEOIMAGE_SAMPLE2 structure [windows Media Format]","wmformat.wmt_videoimage_sample2","wmsdkidl/WMT_VIDEOIMAGE_SAMPLE2"]
old-location: wmformat\wmt_videoimage_sample2.htm
tech.root: wmformat
ms.assetid: 0c4fa9e2-9b7b-4c9e-be58-e28da408337d
ms.date: 4/26/2023
ms.keywords: WMT_VIDEOIMAGE_SAMPLE2, WMT_VIDEOIMAGE_SAMPLE2 structure [windows Media Format], wmformat.wmt_videoimage_sample2, wmsdkidl/WMT_VIDEOIMAGE_SAMPLE2
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMT_VIDEOIMAGE_SAMPLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __WMT_VIDEOIMAGE_SAMPLE2
 - wmsdkidl/__WMT_VIDEOIMAGE_SAMPLE2
 - WMT_VIDEOIMAGE_SAMPLE2
 - wmsdkidl/WMT_VIDEOIMAGE_SAMPLE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_VIDEOIMAGE_SAMPLE2
---

# WMT_VIDEOIMAGE_SAMPLE2 structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_VIDEOIMAGE_SAMPLE2</b> structure describes a sample for a Video Image stream. This structure must be used, either alone or with an accompanying image, in each sample passed to the writer for a Video Image stream. For more information, see <a href="/windows/desktop/wmformat/writing-video-image-samples">Writing Video Image Samples</a>.

## -struct-fields

### -field dwMagic

Reserved. You must set this member to WMT_VIDEOIMAGE_MAGIC_NUMBER_2.

### -field dwStructSize

Size of the structure. Set to <code>sizeof(WMT_VIDEOIMAGE_SAMPLE2)</code>.

### -field dwControlFlags

Specifies the type of sample. Use one or more of the flags in the following table, combined with the bitwise <b>OR</b> operator (|):<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_INPUT_FRAME</td>
<td>Indicates that the sample contains an input image. The image data must be included in the sample immediately following the structure. The format of the image must conform to the values set in the input properties for the stream.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_OUTPUT_FRAME</td>
<td>Indicates that the sample should result in a unique output frame in the stream. If this flag is not set, the remainder of the members of the structure are ignored and the frame in the stream will be a duplicate of the previous frame.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_USES_CURRENT_INPUT_FRAME</td>
<td>Indicates that the sample is based, either solely or in part, on the current  image. If this flag is set, the first set of value members will be used (those with names containing the string "Curr"). 
This flag is not valid unless used in combination with WMT_VIDEOIMAGE_SAMPLE_OUTPUT_FRAME.
</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_USES_PREVIOUS_INPUT_FRAME</td>
<td>Indicates that the sample is based, either solely or in part, on the previous image. If this flag is set, the second set of value members will be used (those with names containing the string "Prev"). 
This flag is not valid unless used in combination with WMT_VIDEOIMAGE_SAMPLE_OUTPUT_FRAME.
</td>
</tr>
</table>

### -field dwViewportWidth

Width of the output frame.

### -field dwViewportHeight

Height of the output frame.

### -field dwCurrImageWidth

Width of the current image.

### -field dwCurrImageHeight

Height of the current image.

### -field fCurrRegionX0

X component of the origin point of the region of interest in the current image.

### -field fCurrRegionY0

Y component of the origin point of the region of interest in the current image.

### -field fCurrRegionWidth

Width of the region of interest in the current image. The specified region of interest will be sized to match the size of the output frame.

### -field fCurrRegionHeight

Height of the region of interest in the current image. The specified region of interest will be sized to match the size of the output frame.

### -field fCurrBlendCoef

Blending coefficient for the current image. This value specifies the transparency of the current image relative to the previous image. The blending coefficients of the two images must total 1.0.

### -field dwPrevImageWidth

Width of the previous image.

### -field dwPrevImageHeight

Height of the previous image.

### -field fPrevRegionX0

X component of the origin point of the region of interest in the previous image.

### -field fPrevRegionY0

Y component of the origin point of the region of interest in the previous image.

### -field fPrevRegionWidth

Width of the region of interest in the previous image. The specified region of interest will be sized to match the size of the output frame.

### -field fPrevRegionHeight

Height of the region of interest in the previous image. The specified region of interest will be sized to match the size of the output frame.

### -field fPrevBlendCoef

Blending coefficient for the previous image. This value specifies the transparency of the previous image relative to the current image. The blending coefficients of the two images must total 1.0.

### -field dwEffectType

The effect identifier of the transition between the previous image and the current image. For more information, see <a href="/windows/desktop/wmformat/video-image-transitions">Video Image Transitions</a>.

### -field dwNumEffectParas

The number of effect parameters relevant to the current effect. The final five members of this structure contain the values of effect parameters. This member specifies how many of those parameters contain valid information.

### -field fEffectPara0

Effect parameter. The uses of this parameter and the other four parameters in this structure are determined by the effect used, as specified by the value of the <b>dwEffectType</b> member.

### -field fEffectPara1

Effect parameter. The uses of this parameter and the other four parameters in this structure are determined by the effect used, as specified by the value of the <b>dwEffectType</b> member.

### -field fEffectPara2

Effect parameter. The uses of this parameter and the other four parameters in this structure are determined by the effect used, as specified by the value of the <b>dwEffectType</b> member.

### -field fEffectPara3

Effect parameter. The uses of this parameter and the other four parameters in this structure are determined by the effect used, as specified by the value of the <b>dwEffectType</b> member.

### -field fEffectPara4

Effect parameter. The uses of this parameter and the other four parameters in this structure are determined by the effect used, as specified by the value of the <b>dwEffectType</b> member.

### -field bKeepPrevImage

For input samples, <b>TRUE</b> indicates that the new image should replace the current image and that the current image should be discarded. The default behavior, indicated by setting this member to <b>FALSE</b>, is for the current image to become the previous image and the new image to become the current image.

## -remarks

When creating an input Video Image sample, the values for the current image describe the image attached to the sample. The values for the previous image describe the image that was the current image in the previous sample. Normally, the previous image is discarded when you pass in a new image. (The old current image becomes the new previous image and the image passed in with the sample becomes the new current image.) If, when passing a new image, you want to discard the old current image and keep the old previous image, you can set the <b>bKeepPrevImage</b> member to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>