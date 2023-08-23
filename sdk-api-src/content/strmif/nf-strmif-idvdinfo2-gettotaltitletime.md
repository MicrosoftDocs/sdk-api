---
UID: NF:strmif.IDvdInfo2.GetTotalTitleTime
title: IDvdInfo2::GetTotalTitleTime (strmif.h)
description: The GetTotalTitleTime method retrieves the total playback time for the current title.
helpviewer_keywords: ["GetTotalTitleTime","GetTotalTitleTime method [DirectShow]","GetTotalTitleTime method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetTotalTitleTime method","IDvdInfo2.GetTotalTitleTime","IDvdInfo2::GetTotalTitleTime","IDvdInfo2GetTotalTitleTime","dshow.idvdinfo2_gettotaltitletime","strmif/IDvdInfo2::GetTotalTitleTime"]
old-location: dshow\idvdinfo2_gettotaltitletime.htm
tech.root: dshow
ms.assetid: 90768da1-592a-49ec-99b0-56f463c322e8
ms.date: 4/26/2023
ms.keywords: GetTotalTitleTime, GetTotalTitleTime method [DirectShow], GetTotalTitleTime method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetTotalTitleTime method, IDvdInfo2.GetTotalTitleTime, IDvdInfo2::GetTotalTitleTime, IDvdInfo2GetTotalTitleTime, dshow.idvdinfo2_gettotaltitletime, strmif/IDvdInfo2::GetTotalTitleTime
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
 - IDvdInfo2::GetTotalTitleTime
 - strmif/IDvdInfo2::GetTotalTitleTime
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
 - IDvdInfo2.GetTotalTitleTime
---

# IDvdInfo2::GetTotalTitleTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetTotalTitleTime</code> method retrieves the total playback time for the current title.

## -parameters

### -param pTotalTime [out]

Pointer to a [DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) structure that receives the total time in hours, minutes, seconds, and frames.

### -param ulTimeCodeFlags [out]

Receives a [DVD_TIMECODE_FLAGS](/windows/desktop/api/strmif/ne-strmif-dvd_timecode_flags) value indicating the frame rate at which the disc was authored to play. Specify <b>NULL</b> if you don't want to receive the timecode information.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
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
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not in the title domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_DVD_NON_ONE_SEQUENTIAL</b></dt>
</dl>
</td>
<td width="60%">
The title is not a one sequential video title, so the timing information might not be continuous.

</td>
</tr>
</table>

## -remarks

The total title time is the time required to play the title sequentially, not counting any stills, pauses, and so on.

This method is for use only with <i>one sequential video titles</i>, which are titles such as movies in which each chapter automatically branches to the next chapter so that the entire title plays continuously without stopping. <i>Nonsequential video titles</i> are titles whose chapters do not automatically play one after another. Because of variations in how DVD authors encode time information on nonsequential video titles, do not use this method to determine the total time for such titles.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>