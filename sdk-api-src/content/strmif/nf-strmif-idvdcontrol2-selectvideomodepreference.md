---
UID: NF:strmif.IDvdControl2.SelectVideoModePreference
title: IDvdControl2::SelectVideoModePreference (strmif.h)
description: The SelectVideoModePreference method sets the specified video mode display (wide screen, letterbox, or pan-scan) for playback.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectVideoModePreference method","IDvdControl2.SelectVideoModePreference","IDvdControl2::SelectVideoModePreference","IDvdControl2SelectVideoModePreference","SelectVideoModePreference","SelectVideoModePreference method [DirectShow]","SelectVideoModePreference method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectvideomodepreference","strmif/IDvdControl2::SelectVideoModePreference"]
old-location: dshow\idvdcontrol2_selectvideomodepreference.htm
tech.root: dshow
ms.assetid: d970f48e-374f-43de-a59c-6c2e70161f55
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectVideoModePreference method, IDvdControl2.SelectVideoModePreference, IDvdControl2::SelectVideoModePreference, IDvdControl2SelectVideoModePreference, SelectVideoModePreference, SelectVideoModePreference method [DirectShow], SelectVideoModePreference method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectvideomodepreference, strmif/IDvdControl2::SelectVideoModePreference
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl2::SelectVideoModePreference
 - strmif/IDvdControl2::SelectVideoModePreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SelectVideoModePreference
---

# IDvdControl2::SelectVideoModePreference


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectVideoModePreference</code> method sets the specified video mode display (wide screen, letterbox, or pan-scan) for playback.

## -parameters

### -param ulPreferredDisplayMode [in]

Value that specifies the new display mode for DVD content. Member of the [DVD_PREFERRED_DISPLAY_MODE](/windows/desktop/api/strmif/ne-strmif-dvd_preferred_display_mode) enumeration.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>

## -remarks

This method changes the default video window's aspect ratio and can also specify a default aspect ratio conversion mechanism.

For anamorphic 16 x 9 source video, formed by stretching the 720 x 480 source video to a 16 x 9 aspect ratio.

<b>Widescreen</b> The 16 x 9 source video should be placed and stretched into the largest 16 x 9 area of the client output window. The highlights are relative to the inside of the 16 x 9 area. Black bars should be added to either the top/bottom or to the sides to maintain a 16 x 9 area.

<b>Pan Scan</b> The video shown is computed by taking a 4 x 3 subwindow from the stretched 16 x 9 video (the horizontal offset is provided in the MPEG-2 video's window's offset). The 4 x 3 subwindow is placed into the largest 4 x 3 area of the output client window. The highlight's coordinates are relative to the 4 x 3 output window (and have no relationship to the source 16 x 9 video). Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area.

<b>Letterbox</b> A 4 x 3 display area is formed by taking the largest 4 x 3 area of the output client window. Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area. The source 16 x 9 video is placed in the largest 16 x 9 subwindow inside of the 4 x 3 subwindow. Black bars should be added to the top and bottom of the subwindow to maintain a 16 x 9 area. The highlight's coordinates are relative to the 4 x 3 subwindow (and have no relationship to the source 16 x 9 video). It is technically possible for a disk to specify a highlight that lies outside of the 16 x 9 area (but still in the 4 x 3 window).

For 4 x 3 video, the video is placed in the largest 4 x 3 output area of the output client window. Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Video_Presentation_Mode_Change</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>