---
UID: NF:strmif.IDvdInfo2.GetKaraokeAttributes
title: IDvdInfo2::GetKaraokeAttributes (strmif.h)
description: The GetKaraokeAttributes method retrieves the karaoke attributes of the specified audio stream in the current title or menu.
helpviewer_keywords: ["GetKaraokeAttributes","GetKaraokeAttributes method [DirectShow]","GetKaraokeAttributes method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetKaraokeAttributes method","IDvdInfo2.GetKaraokeAttributes","IDvdInfo2::GetKaraokeAttributes","IDvdInfo2GetKaraokeAttributes","dshow.idvdinfo2_getkaraokeattributes","strmif/IDvdInfo2::GetKaraokeAttributes"]
old-location: dshow\idvdinfo2_getkaraokeattributes.htm
tech.root: dshow
ms.assetid: c69ea1e0-8d8a-4cd3-86a4-a2d481160a2e
ms.date: 4/26/2023
ms.keywords: GetKaraokeAttributes, GetKaraokeAttributes method [DirectShow], GetKaraokeAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetKaraokeAttributes method, IDvdInfo2.GetKaraokeAttributes, IDvdInfo2::GetKaraokeAttributes, IDvdInfo2GetKaraokeAttributes, dshow.idvdinfo2_getkaraokeattributes, strmif/IDvdInfo2::GetKaraokeAttributes
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
 - IDvdInfo2::GetKaraokeAttributes
 - strmif/IDvdInfo2::GetKaraokeAttributes
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
 - IDvdInfo2.GetKaraokeAttributes
---

# IDvdInfo2::GetKaraokeAttributes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetKaraokeAttributes</code> method retrieves the karaoke attributes of the specified audio stream in the current title or menu.

## -parameters

### -param ulStream [in]

Specifies the index of the audio stream whose attributes you want to query. See Remarks.

### -param pAttributes [out]

Pointer to a [DVD_KaraokeAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_karaokeattributes) structure that is filled with the karaoke attributes.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NOT_IN_KARAOKE_MODE</b></dt>
</dl>
</td>
<td width="60%">
The specified stream is not in karaoke format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not in the title domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The karaoke attributes for the specified stream are not available.

</td>
</tr>
</table>

## -remarks

This method does not explicitly return the number of channels in the stream. You can obtain that information through a call to <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">IDvdInfo2::GetAudioAttributes</a>. This method is demonstrated in the DVDSample application in <b>CKaraokeDlg::DoModal</b>.

The <i>ulStream</i> parameter may be a value from 0 through 7, or one of the following:

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>DVD_STREAM_DATA_CURRENT (0x800)</td>
<td>To query the currently selected audio stream.</td>
</tr>
<tr>
<td>DVD_DEFAULT_AUDIO_STREAM</td>
<td>To query the default audio stream.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>