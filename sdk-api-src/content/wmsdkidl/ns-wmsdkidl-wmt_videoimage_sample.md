---
UID: NS:wmsdkidl.__WMT_VIDEOIMAGE_SAMPLE
title: WMT_VIDEOIMAGE_SAMPLE (wmsdkidl.h)
description: Describes a sample for a Video Image stream that uses the Windows Media Video 9 Image codec.
helpviewer_keywords: ["WMT_VIDEOIMAGE_SAMPLE","WMT_VIDEOIMAGE_SAMPLE structure [windows Media Format]","wmformat.wmt_videoimage_sample","wmsdkidl/WMT_VIDEOIMAGE_SAMPLE"]
old-location: wmformat\wmt_videoimage_sample.htm
tech.root: wmformat
ms.assetid: 8572ca63-760e-4bb8-886e-8e46b8dce9e9
ms.date: 4/26/2023
ms.keywords: WMT_VIDEOIMAGE_SAMPLE, WMT_VIDEOIMAGE_SAMPLE structure [windows Media Format], wmformat.wmt_videoimage_sample, wmsdkidl/WMT_VIDEOIMAGE_SAMPLE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WMT_VIDEOIMAGE_SAMPLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __WMT_VIDEOIMAGE_SAMPLE
 - wmsdkidl/__WMT_VIDEOIMAGE_SAMPLE
 - WMT_VIDEOIMAGE_SAMPLE
 - wmsdkidl/WMT_VIDEOIMAGE_SAMPLE
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
 - WMT_VIDEOIMAGE_SAMPLE
---

# WMT_VIDEOIMAGE_SAMPLE structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[This structure is no longer available for use as of the Windows Media Video 9 Image v2 codec. Instead, use <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2">WMT_VIDEOIMAGE_SAMPLE2</a>.]

The <b>WMT_VIDEOIMAGE_SAMPLE</b> structure describes a sample for a Video Image stream that uses the Windows Media Video 9 Image codec.

## -struct-fields

### -field dwMagic

Reserved value. Always set to WMT_VIDEOIMAGE_MAGIC_NUMBER.

### -field cbStruct

Size of the structure. Always set to <b>sizeof</b>(<b>WMT_VIDEOIMAGE_SAMPLE</b>).

### -field dwControlFlags

One or more of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_INPUT_FRAME</td>
<td>Indicates that the sample contains an input image. The image data must immediately follow the structure in the sample and must conform to the values set in the input properties for the stream.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_OUTPUT_FRAME</td>
<td>Indicates that the sample should result in a unique frame in the stream. If this flag is not set, the remainder of the members of the structure are ignored and the frame in the stream will be identical to the last output stream.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_USES_CURRENT_INPUT_FRAME</td>
<td>Indicates that the sample is based, either solely or in part, on the current image. If this flag is set, the first set of value members will be used. This flag cannot be set if the sample is input only.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_USES_PREVIOUS_INPUT_FRAME</td>
<td>Indicates that the sample is based, either solely or in part, on the previous image. If this flag is set, the second set of value members will be used. This flag cannot be set if the sample is input only.</td>
</tr>
</table>

### -field dwInputFlagsCur

One or more flags indicating the operation to perform on the current image. The following flags are available.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_ADV_BLENDING</td>
<td>Indicates that the sample uses advanced blending. This feature is not supported in the current version.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_BLENDING</td>
<td>Indicates that the sample contains blending. If this flag is set, the sum of the values of <b>lCurBlendCoef1</b> and <b>lPrevBlendCoef1 </b>(before multiplying by the denominator) must equal 1.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_MOTION</td>
<td>Indicates that the sample uses pan and/or zoom.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_ROTATION</td>
<td>Indicates that the sample uses rotation. This feature is not supported in the current version.</td>
</tr>
</table>

### -field lCurMotionXtoX

<b>LONG</b> value containing the horizontal scaling factor of the current image. A scaling factor of 1 means no horizontal scaling will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lCurMotionYtoX

Not used.

### -field lCurMotionXoffset

<b>LONG</b> value containing the horizontal offset for the current image, in pixels, in relation to the last output sample. An offset of 0 means that no panning will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lCurMotionXtoY

Not used.

### -field lCurMotionYtoY

<b>LONG</b> value containing the vertical scaling factor of the current image. A scaling factor of 1 means no vertical scaling will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lCurMotionYoffset

<b>LONG</b> value containing the vertical offset for the current image, in pixels, in relation to the last output sample. An offset of 0 means that no panning will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lCurBlendCoef1

<b>LONG</b> value containing the blend coefficient for the current image when combined with the previous image for an output. This coefficient and the coefficient for the previous image must total 1. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lCurBlendCoef2

Not used.

### -field dwInputFlagsPrev

One or more flags indicating the operation to perform on the previous image. The following flags are available.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_ADV_BLENDING</td>
<td>Indicates that the sample uses advanced blending. This feature is not supported in the current version.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_BLENDING</td>
<td>Indicates that the sample contains blending. If this flag is set, the sum of the values of <b>lCurBlendCoef1</b> and <b>lPrevBlendCoef1 </b>(before multiplying by the denominator) must equal 1.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_MOTION</td>
<td>Indicates that the sample uses pan and/or zoom.</td>
</tr>
<tr>
<td>WMT_VIDEOIMAGE_SAMPLE_ROTATION</td>
<td>Indicates that the sample uses rotation. This feature is not supported in the current version.</td>
</tr>
</table>

### -field lPrevMotionXtoX

<b>LONG</b> value containing the horizontal scaling factor of the previous image. A scaling factor of 1 means no horizontal scaling will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lPrevMotionYtoX

Not used.

### -field lPrevMotionXoffset

<b>LONG</b> value containing the horizontal offset for the previous image, in pixels, in relation to the last output sample. An offset of 0 means that no panning will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lPrevMotionXtoY

Not used.

### -field lPrevMotionYtoY

<b>LONG</b> value containing the vertical scaling factor of the previous image. A scaling factor of 1 means no vertical scaling will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lPrevMotionYoffset

<b>LONG</b> value containing the vertical offset for the previous image, in pixels, in relation to the last output sample. An offset of 0 means that no panning will be performed for this sample. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lPrevBlendCoef1

<b>LONG</b> value containing the blend coefficient for the previous image when combined with the current image for an output. This coefficient and the coefficient for the current image must total 1. This value must be multiplied by WMT_VIDEOIMAGE_INTEGER_DENOMINATOR before being set in the structure.

### -field lPrevBlendCoef2

Not used.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>