---
UID: NF:strmif.IDvdInfo2.GetCurrentLocation
title: IDvdInfo2::GetCurrentLocation (strmif.h)
description: The GetCurrentLocation method retrieves the current playback location.
helpviewer_keywords: ["GetCurrentLocation","GetCurrentLocation method [DirectShow]","GetCurrentLocation method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentLocation method","IDvdInfo2.GetCurrentLocation","IDvdInfo2::GetCurrentLocation","IDvdInfo2GetCurrentLocation","dshow.idvdinfo2_getcurrentlocation","strmif/IDvdInfo2::GetCurrentLocation"]
old-location: dshow\idvdinfo2_getcurrentlocation.htm
tech.root: dshow
ms.assetid: 54005c07-1689-411c-88a9-bcd19cc065dd
ms.date: 4/26/2023
ms.keywords: GetCurrentLocation, GetCurrentLocation method [DirectShow], GetCurrentLocation method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentLocation method, IDvdInfo2.GetCurrentLocation, IDvdInfo2::GetCurrentLocation, IDvdInfo2GetCurrentLocation, dshow.idvdinfo2_getcurrentlocation, strmif/IDvdInfo2::GetCurrentLocation
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
 - IDvdInfo2::GetCurrentLocation
 - strmif/IDvdInfo2::GetCurrentLocation
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
 - IDvdInfo2.GetCurrentLocation
---

# IDvdInfo2::GetCurrentLocation


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentLocation</code> method retrieves the current playback location.

## -parameters

### -param pLocation [out]

Pointer to a variable of type [DVD_PLAYBACK_LOCATION2](/windows/desktop/api/strmif/ns-strmif-dvd_playback_location2) that receives the playback location information.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pLocation</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is in an invalid domain.

</td>
</tr>
</table>

## -remarks

This method retrieves information sufficient to restart playback of a video from the current playback location in titles that don't explicitly disable seeking to the current location. After the disc has been ejected, the information returned by this method will not necessarily be sufficient to restart playback. To save the current location and state information to disc so that the user can return to the same location at any later time, use <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">GetState</a>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>