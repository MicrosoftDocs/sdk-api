---
UID: NF:strmif.IDvdInfo.GetTotalTitleTime
title: IDvdInfo::GetTotalTitleTime (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the total playback time for the current title.
helpviewer_keywords: ["GetTotalTitleTime","GetTotalTitleTime method [DirectShow]","GetTotalTitleTime method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetTotalTitleTime method","IDvdInfo.GetTotalTitleTime","IDvdInfo::GetTotalTitleTime","IDvdInfoGetTotalTitleTime","dshow.idvdinfo_gettotaltitletime","strmif/IDvdInfo::GetTotalTitleTime"]
old-location: dshow\idvdinfo_gettotaltitletime.htm
tech.root: dshow
ms.assetid: 90f3a053-edc8-4e42-ae00-31d66d9e3115
ms.date: 4/26/2023
ms.keywords: GetTotalTitleTime, GetTotalTitleTime method [DirectShow], GetTotalTitleTime method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetTotalTitleTime method, IDvdInfo.GetTotalTitleTime, IDvdInfo::GetTotalTitleTime, IDvdInfoGetTotalTitleTime, dshow.idvdinfo_gettotaltitletime, strmif/IDvdInfo::GetTotalTitleTime
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo::GetTotalTitleTime
 - strmif/IDvdInfo::GetTotalTitleTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetTotalTitleTime
---

# IDvdInfo::GetTotalTitleTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the total playback time for the current title.

## -parameters

### -param pulTotalTime [out]

Pointer to the total time in [DVD_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_timecode) format, which includes hours, minutes, seconds, and frames.

## -returns

Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

The method is restricted to simple linear movies by design.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>