---
UID: NE:strmif.tagDVD_PREFERRED_DISPLAY_MODE
title: DVD_PREFERRED_DISPLAY_MODE (strmif.h)
description: Indicates the user's preferred window aspect ratio and conversion method.
helpviewer_keywords: ["DISPLAY_16x9","DISPLAY_4x3_LETTERBOX_PREFERRED","DISPLAY_4x3_PANSCAN_PREFERRED","DISPLAY_CONTENT_DEFAULT","DVD_PREFERRED_DISPLAY_MODE","DVD_PREFERRED_DISPLAY_MODE","DVD_PREFERRED_DISPLAY_MODE enumeration [DirectShow]","DVD_PREFERRED_DISPLAY_MODEEnumeration","dshow.dvd_preferred_display_mode","strmif/DISPLAY_16x9","strmif/DISPLAY_4x3_LETTERBOX_PREFERRED","strmif/DISPLAY_4x3_PANSCAN_PREFERRED","strmif/DISPLAY_CONTENT_DEFAULT","strmif/DVD_PREFERRED_DISPLAY_MODE"]
old-location: dshow\dvd_preferred_display_mode.htm
tech.root: dshow
ms.assetid: afb235ae-ba60-491f-8b88-7fe824f00f77
ms.date: 4/26/2023
ms.keywords: DISPLAY_16x9, DISPLAY_4x3_LETTERBOX_PREFERRED, DISPLAY_4x3_PANSCAN_PREFERRED, DISPLAY_CONTENT_DEFAULT, DVD_PREFERRED_DISPLAY_MODE, DVD_PREFERRED_DISPLAY_MODE , DVD_PREFERRED_DISPLAY_MODE enumeration [DirectShow], DVD_PREFERRED_DISPLAY_MODEEnumeration, dshow.dvd_preferred_display_mode, strmif/DISPLAY_16x9, strmif/DISPLAY_4x3_LETTERBOX_PREFERRED, strmif/DISPLAY_4x3_PANSCAN_PREFERRED, strmif/DISPLAY_CONTENT_DEFAULT, strmif/DVD_PREFERRED_DISPLAY_MODE
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
req.typenames: DVD_PREFERRED_DISPLAY_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_PREFERRED_DISPLAY_MODE
 - strmif/tagDVD_PREFERRED_DISPLAY_MODE
 - DVD_PREFERRED_DISPLAY_MODE
 - strmif/DVD_PREFERRED_DISPLAY_MODE
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
 - DVD_PREFERRED_DISPLAY_MODE
---

# DVD_PREFERRED_DISPLAY_MODE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  Deprecated.</div><div> </div>
Indicates the user's preferred window aspect ratio and conversion method.

## -enum-fields

### -field DISPLAY_CONTENT_DEFAULT:0

Use the default window size and content type.

### -field DISPLAY_16x9:1

Use a 16 x 9 window.

### -field DISPLAY_4x3_PANSCAN_PREFERRED:2

Use a 4 x 3 window and convert to pan-scan, if possible.

### -field DISPLAY_4x3_LETTERBOX_PREFERRED:3

Use a 4 x 3 window and convert to letterbox, if possible.

## -remarks

The <b>DVD_PREFERRED_DISPLAY_MODE</b> enumeration indicates the user's preferred window aspect ratio and preferred method of conversion of 16 x 9 content to a 4 x 3 window aspect ratio. Pan-scan and letterboxing are the two conversion methods. Displaying a video at the largest possible size inside the display window without any cropping or stretching is called displaying in letterbox format. <i>Pan-scan</i> is specifically cropping a 16 x 9 video for display in a 4 x 3 window using parameters defined by the video author.

This enumerated type indicates a preference of conversion mechanisms because some content can only be displayed using one of these methods. Content that is 4 x 3 is always converted to a 16 x 9 window by using sideboxing, where black bars are added to the right and left sides of the display instead of the top and bottom of the display as in the 16 x 9 to 4 x 3 conversion using letterboxing.

The following table shows the conversion method used between the actual content type listed in the first column, and the user display preference setting, indicated by one of the other columns.

<table>
<tr>
<th>Actual content type
            </th>
<th>16 x 9
            </th>
<th>4 x 3 pan-scan
            </th>
<th>4 x 3 letterbox
            </th>
</tr>
<tr>
<td>4 x 3</td>
<td>Sideboxing</td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td>16 x 9 letterbox only</td>
<td>None</td>
<td>Letterbox</td>
<td>Letterbox</td>
</tr>
<tr>
<td>16 x 9 pan-scan only</td>
<td>None</td>
<td>Pan-scan</td>
<td>Pan-scan</td>
</tr>
<tr>
<td>16 x 9 pan-scan or letterbox</td>
<td>None</td>
<td>Pan-scan</td>
<td>Letterbox</td>
</tr>
</table>
 

The native window size used is always the user's preferred size.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-videomodepreferrence">IDvdControl::VideoModePreferrence</a>
