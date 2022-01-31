---
UID: NE:dxva2api._DXVA2_SampleFormat
title: DXVA2_SampleFormat (dxva2api.h)
description: Describes the content of a video sample. These flags are used in the DXVA2_ExtendedFormat structure.
helpviewer_keywords: ["7d2d38c0-249d-47c3-acda-ba1bec721a5c","DXVA2_SampleFieldInterleavedEvenFirst","DXVA2_SampleFieldInterleavedOddFirst","DXVA2_SampleFieldSingleEven","DXVA2_SampleFieldSingleOdd","DXVA2_SampleFormat","DXVA2_SampleFormat enumeration [Media Foundation]","DXVA2_SampleFormatMask","DXVA2_SampleProgressiveFrame","DXVA2_SampleSubStream","DXVA2_SampleUnknown","dxva2api/DXVA2_SampleFieldInterleavedEvenFirst","dxva2api/DXVA2_SampleFieldInterleavedOddFirst","dxva2api/DXVA2_SampleFieldSingleEven","dxva2api/DXVA2_SampleFieldSingleOdd","dxva2api/DXVA2_SampleFormat","dxva2api/DXVA2_SampleFormatMask","dxva2api/DXVA2_SampleProgressiveFrame","dxva2api/DXVA2_SampleSubStream","dxva2api/DXVA2_SampleUnknown","mf.dxva2_sampleformat"]
old-location: mf\dxva2_sampleformat.htm
tech.root: mf
ms.assetid: 7d2d38c0-249d-47c3-acda-ba1bec721a5c
ms.date: 12/05/2018
ms.keywords: 7d2d38c0-249d-47c3-acda-ba1bec721a5c, DXVA2_SampleFieldInterleavedEvenFirst, DXVA2_SampleFieldInterleavedOddFirst, DXVA2_SampleFieldSingleEven, DXVA2_SampleFieldSingleOdd, DXVA2_SampleFormat, DXVA2_SampleFormat enumeration [Media Foundation], DXVA2_SampleFormatMask, DXVA2_SampleProgressiveFrame, DXVA2_SampleSubStream, DXVA2_SampleUnknown, dxva2api/DXVA2_SampleFieldInterleavedEvenFirst, dxva2api/DXVA2_SampleFieldInterleavedOddFirst, dxva2api/DXVA2_SampleFieldSingleEven, dxva2api/DXVA2_SampleFieldSingleOdd, dxva2api/DXVA2_SampleFormat, dxva2api/DXVA2_SampleFormatMask, dxva2api/DXVA2_SampleProgressiveFrame, dxva2api/DXVA2_SampleSubStream, dxva2api/DXVA2_SampleUnknown, mf.dxva2_sampleformat
req.header: dxva2api.h
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
req.typenames: DXVA2_SampleFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_SampleFormat
 - dxva2api/_DXVA2_SampleFormat
 - DXVA2_SampleFormat
 - dxva2api/DXVA2_SampleFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_SampleFormat
---

# DXVA2_SampleFormat enumeration


## -description

Describes the content of a video sample. These flags are used in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.

## -enum-fields

### -field DXVA2_SampleFormatMask:0xff

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_SampleUnknown:0

Unknown format. Default to DXVA2_SampleProgressiveFrame.

### -field DXVA2_SampleProgressiveFrame:2

The sample contains a progressive (non-interlaced) frame.

### -field DXVA2_SampleFieldInterleavedEvenFirst:3

The sample contains two interleaved fields. The even field should be displayed first.

### -field DXVA2_SampleFieldInterleavedOddFirst:4

The sample contains two interleaved fields. The odd field should be displayed first.

### -field DXVA2_SampleFieldSingleEven:5

The sample contains a single even field.

### -field DXVA2_SampleFieldSingleOdd:6

The sample contains a single odd field.

### -field DXVA2_SampleSubStream:7

The sample contains a video substream frame. Use this value for substream mixing.

## -remarks

This enumeration is equivalent to the <b>DXVA_SampleFormat</b> enumeration used in DXVA 1.0.

The following table shows the mapping from <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode">MFVideoInterlaceMode</a> enumeration values, which are used in Media Foundation media types, to <b>DXVA2_SampleFormat</b> values.

<table>
<tr>
<th>MFVideoInterlaceMode Value</th>
<th>DXVA2_SampleFormat Value</th>
</tr>
<tr>
<td>MFVideoInterlace_Unknown</td>
<td>DXVA2_SampleUnknown.</td>
</tr>
<tr>
<td>MFVideoInterlace_Progressive</td>
<td>DXVA2_SampleProgressiveFrame.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldInterleavedUpperFirst</td>
<td>DXVA2_SampleFieldInterleavedEvenFirst</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldInterleavedLowerFirst</td>
<td>DXVA2_SampleFieldInterleavedOddFirst.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldSingleUpper</td>
<td>DXVA2_SampleFieldSingleEven.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldSingleLower</td>
<td>DXVA2_SampleFieldSingleOdd.</td>
</tr>
<tr>
<td>MFVideoInterlace_MixedInterlaceOrProgressive</td>
<td>No exact match. Use DXVA2_SampleFieldInterleavedEvenFirst as an initial value, then use the interlace flags from the media samples. For more information, see <a href="/windows/desktop/medfound/video-interlacing">Video Interlacing</a>.</td>
</tr>
</table>
 

With the exception of MFVideoInterlace_MixedInterlaceOrProgressive, each pair of corresponding enumeration values has the same numeric value.

The value DXVA2_SampleSubStream has no equivalent in the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode">MFVideoInterlaceMode</a> enumeration.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
