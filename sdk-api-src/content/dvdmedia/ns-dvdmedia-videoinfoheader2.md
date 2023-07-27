---
UID: NS:dvdmedia.tagVIDEOINFOHEADER2
title: VIDEOINFOHEADER2 (dvdmedia.h)
description: The VIDEOINFOHEADER2 structure describes the bitmap and color information for a video image, including interlace, copy protection, and pixel aspect ratio information.
helpviewer_keywords: ["AMCONTROL_COLORINFO_PRESENT","AMCONTROL_PAD_TO_16x9","AMCONTROL_PAD_TO_4x3","AMCONTROL_USED","AMINTERLACE_1FieldPerSample","AMINTERLACE_DisplayModeBobOnly","AMINTERLACE_DisplayModeBobOrWeave","AMINTERLACE_DisplayModeWeaveOnly","AMINTERLACE_Field1First","AMINTERLACE_FieldPatBothIrregular","AMINTERLACE_FieldPatBothRegular","AMINTERLACE_FieldPatField1Only","AMINTERLACE_FieldPatField2Only","AMINTERLACE_IsInterlaced","VIDEOINFOHEADER2","VIDEOINFOHEADER2 structure [DirectShow]","VIDEOINFOHEADER2Structure","dshow.videoinfoheader2","dvdmedia/VIDEOINFOHEADER2","tagVIDEOINFOHEADER2"]
old-location: dshow\videoinfoheader2.htm
tech.root: dshow
ms.assetid: 5e3d5bf0-435f-45da-8409-a1463b56a7ae
ms.date: 4/26/2023
ms.keywords: AMCONTROL_COLORINFO_PRESENT, AMCONTROL_PAD_TO_16x9, AMCONTROL_PAD_TO_4x3, AMCONTROL_USED, AMINTERLACE_1FieldPerSample, AMINTERLACE_DisplayModeBobOnly, AMINTERLACE_DisplayModeBobOrWeave, AMINTERLACE_DisplayModeWeaveOnly, AMINTERLACE_Field1First, AMINTERLACE_FieldPatBothIrregular, AMINTERLACE_FieldPatBothRegular, AMINTERLACE_FieldPatField1Only, AMINTERLACE_FieldPatField2Only, AMINTERLACE_IsInterlaced, VIDEOINFOHEADER2, VIDEOINFOHEADER2 structure [DirectShow], VIDEOINFOHEADER2Structure, dshow.videoinfoheader2, dvdmedia/VIDEOINFOHEADER2, tagVIDEOINFOHEADER2
req.header: dvdmedia.h
req.include-header: 
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
req.typenames: VIDEOINFOHEADER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVIDEOINFOHEADER2
 - dvdmedia/tagVIDEOINFOHEADER2
 - VIDEOINFOHEADER2
 - dvdmedia/VIDEOINFOHEADER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - VIDEOINFOHEADER2
---

# VIDEOINFOHEADER2 structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VIDEOINFOHEADER2</b> structure describes the bitmap and color information for a video image, including interlace, copy protection, and pixel aspect ratio information.

## -struct-fields

### -field rcSource

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies what part of the source stream should be used to fill the destination buffer. Renderers can use this field to ask the decoders to stretch or clip. For more information, see <a href="/windows/desktop/DirectShow/source-and-target-rectangles-in-video-renderers">Source and Target Rectangles in Video Renderers</a>.

### -field rcTarget

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies that specifies what part of the destination buffer should be used

### -field dwBitRate

The approximate data rate of the video stream, in bits per second.

### -field dwBitErrorRate

The data error rate of the video stream, in bits per second.

### -field AvgTimePerFrame

The video frame's average display time, in 100-nanosecond units. For more information, see the Remarks section for the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

### -field dwInterlaceFlags

Flags that specify how the video is interlaced. This member is a bit-wise combination of zero or more of the following flags. The flags in Group 2 are mutually exclusive, and so are the flags in Group 3. (The flags in Group 2 are not recommended.) The flags in Group 1 may be combined with each other, and with one flag each from Group 2 and Group 3. See the table at the bottom of this page for more information about flag combinations.

<table>
<tr>
<th>Group 1</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_IsInterlaced"></a><a id="aminterlace_isinterlaced"></a><a id="AMINTERLACE_ISINTERLACED"></a><dl>
<dt><b>AMINTERLACE_IsInterlaced</b></dt>
</dl>
</td>
<td width="60%">
The stream is interlaced. If this flag is absent, the video is progressive and the other bits are irrelevant.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_1FieldPerSample"></a><a id="aminterlace_1fieldpersample"></a><a id="AMINTERLACE_1FIELDPERSAMPLE"></a><dl>
<dt><b>AMINTERLACE_1FieldPerSample</b></dt>
</dl>
</td>
<td width="60%">
Each media sample contains one field. If this flag is absent, each media sample contains two fields.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_Field1First"></a><a id="aminterlace_field1first"></a><a id="AMINTERLACE_FIELD1FIRST"></a><dl>
<dt><b>AMINTERLACE_Field1First</b></dt>
</dl>
</td>
<td width="60%">
Field 1 is first. If this flag is absent, field 2 is first. (The top field in PAL is field 1, and the top field in NTSC is field 2.)

</td>
</tr>
</table>
 

<table>
<tr>
<th>Group 2</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_FieldPatField1Only"></a><a id="aminterlace_fieldpatfield1only"></a><a id="AMINTERLACE_FIELDPATFIELD1ONLY"></a><dl>
<dt><b>AMINTERLACE_FieldPatField1Only</b></dt>
</dl>
</td>
<td width="60%">
The stream never contains a field 2.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_FieldPatField2Only"></a><a id="aminterlace_fieldpatfield2only"></a><a id="AMINTERLACE_FIELDPATFIELD2ONLY"></a><dl>
<dt><b>AMINTERLACE_FieldPatField2Only</b></dt>
</dl>
</td>
<td width="60%">
The stream never contains a field 1.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_FieldPatBothRegular"></a><a id="aminterlace_fieldpatbothregular"></a><a id="AMINTERLACE_FIELDPATBOTHREGULAR"></a><dl>
<dt><b>AMINTERLACE_FieldPatBothRegular</b></dt>
</dl>
</td>
<td width="60%">
There is one field 2 for every field 1.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_FieldPatBothIrregular"></a><a id="aminterlace_fieldpatbothirregular"></a><a id="AMINTERLACE_FIELDPATBOTHIRREGULAR"></a><dl>
<dt><b>AMINTERLACE_FieldPatBothIrregular</b></dt>
</dl>
</td>
<td width="60%">
The stream contains an irregular pattern of field 1 and field 2.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Group 3</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_DisplayModeBobOnly"></a><a id="aminterlace_displaymodebobonly"></a><a id="AMINTERLACE_DISPLAYMODEBOBONLY"></a><dl>
<dt><b>AMINTERLACE_DisplayModeBobOnly</b></dt>
</dl>
</td>
<td width="60%">
Bob display mode only.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_DisplayModeWeaveOnly"></a><a id="aminterlace_displaymodeweaveonly"></a><a id="AMINTERLACE_DISPLAYMODEWEAVEONLY"></a><dl>
<dt><b>AMINTERLACE_DisplayModeWeaveOnly</b></dt>
</dl>
</td>
<td width="60%">
Weave display mode only.

</td>
</tr>
<tr>
<td width="40%"><a id="AMINTERLACE_DisplayModeBobOrWeave"></a><a id="aminterlace_displaymodeboborweave"></a><a id="AMINTERLACE_DISPLAYMODEBOBORWEAVE"></a><dl>
<dt><b>AMINTERLACE_DisplayModeBobOrWeave</b></dt>
</dl>
</td>
<td width="60%">
Either bob or weave mode.

</td>
</tr>
</table>
 

Set undefined flags to zero, or the connection will be rejected.

### -field dwCopyProtectFlags

Flag set with the AMCOPYPROTECT_RestrictDuplication value (0x00000001) to indicate that the duplication of the stream should be restricted. If undefined, specify zero or else the connection will be rejected.

### -field dwPictAspectRatioX

The X dimension of picture aspect ratio. For example, 16 for a 16-inch x 9-inch display.

### -field dwPictAspectRatioY

The Y dimension of picture aspect ratio. For example, 9 for a 16-inch x 9-inch display.

### -field dwControlFlags

This field was originally named <b>dwReserved</b>, and was required to be zero. The field was renamed to <b>dwControlFlags</b>, and must contain a bitwise OR of zero or more of the following flags:


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AMCONTROL_USED"></a><a id="amcontrol_used"></a><dl>
<dt><b>AMCONTROL_USED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the dwControlFlags flags are used.

</td>
</tr>
<tr>
<td width="40%"><a id="AMCONTROL_PAD_TO_4x3"></a><a id="amcontrol_pad_to_4x3"></a><a id="AMCONTROL_PAD_TO_4X3"></a><dl>
<dt><b>AMCONTROL_PAD_TO_4x3</b></dt>
</dl>
</td>
<td width="60%">
The image should be padded and displayed in a 4 x 3 area.

</td>
</tr>
<tr>
<td width="40%"><a id="AMCONTROL_PAD_TO_16x9"></a><a id="amcontrol_pad_to_16x9"></a><a id="AMCONTROL_PAD_TO_16X9"></a><dl>
<dt><b>AMCONTROL_PAD_TO_16x9</b></dt>
</dl>
</td>
<td width="60%">
The image should be padded and displayed in a 16 x 9 area.

</td>
</tr>
<tr>
<td width="40%"><a id="AMCONTROL_COLORINFO_PRESENT"></a><a id="amcontrol_colorinfo_present"></a><dl>
<dt><b>AMCONTROL_COLORINFO_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
Additional color information is contained in the upper 24 bits of the <b>dwControlFlags</b> field.

</td>
</tr>
</table>
 

The AMCONTROL_USED flag provides backward compatibility with older filters. If the AMCONTROL_USED flag is not set, the remaining bits in this field should be ignored. If a filter uses any of the other flags, it should set the AMCONTROL_USED flag.

The two AMCONTROL_PAD_xxx flags are used by decoders to determine the aspect ratio of the output rectangle. The source filter sets the AMCONTROL_USED flag and one of the padding flags and calls <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryaccept">QueryAccept</a> on the downstream pin. If the decoder rejects the type, the source filter should set the dwControlFlags field to zero. For more information on the use of these flags, see MPEG Decoder Preprocessing Transformations.

If the AMCONTROL_COLORINFO_PRESENT flag is set, it means the upper 24 bits of the dwControlFlags field are treated as a <b>DXVA_ExtendedFormat</b> structure. See Remarks for more information.

If this field contains any combination of flags that the filter does not support, the filter should reject the media type.

### -field dwReserved1

See description of <b>dwControlFlags</b>.

### -field dwReserved2

Reserved for future use. Must be zero.

### -field bmiHeader

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains color and dimension information for the video image bitmap.

When used inside a <b>VIDEOINFOHEADER2</b> structure, the semantics of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure differ slightly from how the structure is used in GDI. For more information, refer to the topic <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>.

## -remarks

The picture aspect ratio is given by <b>dwPictAspectRatioX</b> and <b>dwPictAspectRatioY</b>. These specify the intended shape of the video image when it is displayed. The pixel aspect ratio is calculated from the <b>rcSource</b> rectangle and the picture aspect ratio.

The <b>dwInterlaceFlags</b> field indicates whether the video is interlaced, and if so, the format of the fields within the media samples. The following table shows the valid interlace modes for the Overlay Mixer and Video Mixing Renderer filters.

<table>
<tr>
<th>Display Mode
            </th>
<th>Interlace Flags
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>Progressive frames</td>
<td>None</td>
<td>The video stream is not interlaced.</td>
</tr>
<tr>
<td>Non-interleaved bob</td>
<td>AMINTERLACE_IsInterlaced |AMINTERLACE_1FieldPerSample |

AMINTERLACE_DisplayModeBobOnly

</td>
<td>The entire video stream is interlaced, and each media sample contains a single video field.</td>
</tr>
<tr>
<td>Interleaved bob</td>
<td>AMINTERLACE_IsInterlaced |AMINTERLACE_DisplayModeBobOnly

</td>
<td>The entire video stream is interlaced. Each media sample contains two video fields. Flags on the media sample indicate which field to display first.</td>
</tr>
<tr>
<td>Weave</td>
<td>AMINTERLACE_IsInterlaced |AMINTERLACE_FieldPatBothRegular |

AMINTERLACE_DisplayModeWeaveOnly

</td>
<td>The video stream is interlaced, and each sample contains two video fields. The fields should not be deinterlaced.</td>
</tr>
<tr>
<td>Bob or weave</td>
<td>AMINTERLACE_IsInterlaced |AMINTERLACE_DisplayModeBobOrWeave

</td>
<td>The video stream varies between progressive and interlaced content. Each media sample contains either a progressive frame or two video fields. Flags on the media sample indicate the correct way to display the contents.</td>
</tr>
</table>
 

If the video is interlaced, the media samples may carry flags that describe the contents of the sample (such as field 1 or field 2), along with the rendering requirements. These are specified by setting the <b>dwTypeSpecificFlags</b> member of each media sample's <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties">AM_SAMPLE2_PROPERTIES</a> structure. The following table shows the valid media sample flags for each of the display modes listed in the previous table. To set these flags, call <a href="/windows/desktop/api/strmif/nf-strmif-imediasample2-setproperties">IMediaSample2::SetProperties</a> on the media sample.

<table>
<tr>
<th colspan="2">Display Mode</th>
<th>Media Sample Properties</th>
</tr>
<tr>
<td colspan="2">Progressive frames</td>
<td>None</td>
</tr>
<tr>
<td colspan="2">Non-interleaved bob</td>
<td>AM_VIDEO_FLAG_FIELD1 or AM_VIDEO_FLAG_FIELD2</td>
</tr>
<tr>
<td rowspan="2">Interleaved bob</td>
<td>Field 1 first</td>
<td>AM_VIDEO_FLAG_FIELD1FIRST</td>
</tr>
<tr>
<td>Field 2 first</td>
<td>None</td>
</tr>
<tr>
<td colspan="2">Weave</td>
<td>AM_VIDEO_FLAG_WEAVE</td>
</tr>
<tr>
<td rowspan="3">Bob or weave</td>
<td>Bob, field 1 first</td>
<td>AM_VIDEO_FLAG_FIELD1FIRST</td>
</tr>
<tr>
<td>Bob, field 2 first</td>
<td>None</td>
</tr>
<tr>
<td>Weave</td>
<td>AM_VIDEO_FLAG_WEAVE</td>
</tr>
</table>
 

Use the bit mask AMINTERLACE_FieldPatternMask to check the field pattern flags in <b>dwInterlaceFlags</b>:


```cpp

switch (dwInterlaceFlags & AMINTERLACE_FieldPatternMask)
{
case AMINTERLACE_FieldPatField1Only:
    // Stream never contains a Field 2.

case AMINTERLACE_FieldPatField2Only:
    // Stream never contains a Field 1.

case AMINTERLACE_FieldPatBothRegular:
    // One Field 2 for every Field 1.

case AMINTERLACE_FieldPatBothIrregular:
    // Random pattern of Field 1 and Field 2.
}

```


Use the bit mask AMINTERLACE_DisplayModeMask to check the display mode flags in <b>dwInterlaceFlags</b>:


```cpp

switch (dwInterlaceFlags & AMINTERLACE_DisplayModeMask)
{
case AMINTERLACE_DisplayModeBobOnly:
    // Bob display mode only.

case AMINTERLACE_DisplayModeWeaveOnly:
    // Weave display mode only.

case AMINTERLACE_DisplayModeBobOrWeave:
    // Either bob or weave mode.
}

```


Interlaced video samples must have valid time stamps. Otherwise, it is not guaranteed that the display driver can deinterlace the video. If you need to display an interlaced video frame with no time stamp, set the AM_VIDEO_FLAG_WEAVE flag on the sample as follows:


```cpp

IMediaSample2* pSample2 = NULL;
hr = pSample->QueryInterface(IID_IMediaSample2, (void**)&pSample2);
if (SUCCEEDED(hr))
{
    AM_SAMPLE2_PROPERTIES Prop;
    hr = pSample2->GetProperties(sizeof(Prop), (BYTE*)&Prop);
    if (SUCCEEDED(hr))
    {
        Prop.dwTypeSpecificFlags = AM_VIDEO_FLAG_WEAVE;
        hr = pSample2->SetProperties(sizeof(Prop), (BYTE*)&Prop);
    }
    pSample2->Release();
}

```


This causes the driver to display the two fields as one frame, using weave mode, without deinterlacing.

<h3><a id="Extended_Color_Information"></a><a id="extended_color_information"></a><a id="EXTENDED_COLOR_INFORMATION"></a>Extended Color Information</h3>
If the AMCONTROL_COLORINFO_PRESENT flag is set in the <b>dwControlFlags</b> member, you can cast the <b>dwControlFlags</b> value to a <b>DXVA_ExtendedFormat</b> structure to access the extended color information, as shown in the following code.


```cpp

VIDEOINFOHEADER2 *pVIH2;
DXVA_ExtendedFormat& flags = (DXVA_ExtendedFormat&)pVIH2->dwControlFlags;

```


Ignore the <b>SampleFormat</b> member of the <b>DXVA_ExtendedFormat</b> structure, because it corresponds to the lower 8 bits of <b>dwControlFlags</b>, which are reserved for the AMCONTROL_xxx flags. The <b>DXVA_ExtendedFormat</b> structure is documented in the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/media-types">Media Types</a>