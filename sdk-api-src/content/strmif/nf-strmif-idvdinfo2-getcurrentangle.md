---
UID: NF:strmif.IDvdInfo2.GetCurrentAngle
title: IDvdInfo2::GetCurrentAngle (strmif.h)
description: The GetCurrentAngle method retrieves the number of available angles in the current angle block and the currently selected angle number.
helpviewer_keywords: ["GetCurrentAngle","GetCurrentAngle method [DirectShow]","GetCurrentAngle method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentAngle method","IDvdInfo2.GetCurrentAngle","IDvdInfo2::GetCurrentAngle","IDvdInfo2GetCurrentAngle","dshow.idvdinfo2_getcurrentangle","strmif/IDvdInfo2::GetCurrentAngle"]
old-location: dshow\idvdinfo2_getcurrentangle.htm
tech.root: dshow
ms.assetid: 9347cad1-f061-45e9-ab4a-66e87a2b0c86
ms.date: 4/26/2023
ms.keywords: GetCurrentAngle, GetCurrentAngle method [DirectShow], GetCurrentAngle method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentAngle method, IDvdInfo2.GetCurrentAngle, IDvdInfo2::GetCurrentAngle, IDvdInfo2GetCurrentAngle, dshow.idvdinfo2_getcurrentangle, strmif/IDvdInfo2::GetCurrentAngle
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
 - IDvdInfo2::GetCurrentAngle
 - strmif/IDvdInfo2::GetCurrentAngle
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
 - IDvdInfo2.GetCurrentAngle
---

# IDvdInfo2::GetCurrentAngle


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentAngle</code> method retrieves the number of available angles in the current angle block and the currently selected angle number.

## -parameters

### -param pulAnglesAvailable [out]

Receives the number of available angles. There are up to nine angles in an angle block, numbered 1 through 9. If the value equals 1, then the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not in an angle block.

### -param pulCurrentAngle [out]

Receives the current angle number.

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
DVD Navigator is not initialized or not in a valid domain.

</td>
</tr>
</table>

## -remarks

Note that angle and menu button indexes are 1-based, while audio and subpicture stream indexes are 0-based. When the DVD Navigator is about to enter an angle block, it sends the application an <a href="/windows/desktop/DirectShow/ec-dvd-angles-available">EC_DVD_ANGLES_AVAILABLE</a> event notification with the <i>lParam</i> set to 1. Applications will typically call <code>GetCurrentAngle</code> and <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectangle">IDvdControl2::SelectAngle</a> within their event handler for EC_DVD_ANGLES_AVAILABLE.

This method is demonstrated in the DVDSample application in <b>CAngleDlg::MakeAngleList</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-angles-available">EC_DVD_ANGLES_AVAILABLE</a>



<a href="/windows/desktop/DirectShow/ec-dvd-angle-change">EC_DVD_ANGLE_CHANGE</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>