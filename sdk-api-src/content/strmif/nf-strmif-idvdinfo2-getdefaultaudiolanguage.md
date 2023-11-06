---
UID: NF:strmif.IDvdInfo2.GetDefaultAudioLanguage
title: IDvdInfo2::GetDefaultAudioLanguage (strmif.h)
description: The GetDefaultAudioLanguage method retrieves the default audio language.
helpviewer_keywords: ["GetDefaultAudioLanguage","GetDefaultAudioLanguage method [DirectShow]","GetDefaultAudioLanguage method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDefaultAudioLanguage method","IDvdInfo2.GetDefaultAudioLanguage","IDvdInfo2::GetDefaultAudioLanguage","IDvdInfo2GetDefaultAudioLanguage","dshow.idvdinfo2_getdefaultaudiolanguage","strmif/IDvdInfo2::GetDefaultAudioLanguage"]
old-location: dshow\idvdinfo2_getdefaultaudiolanguage.htm
tech.root: dshow
ms.assetid: 89f93521-9df7-4162-bb66-2210cceebc75
ms.date: 4/26/2023
ms.keywords: GetDefaultAudioLanguage, GetDefaultAudioLanguage method [DirectShow], GetDefaultAudioLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDefaultAudioLanguage method, IDvdInfo2.GetDefaultAudioLanguage, IDvdInfo2::GetDefaultAudioLanguage, IDvdInfo2GetDefaultAudioLanguage, dshow.idvdinfo2_getdefaultaudiolanguage, strmif/IDvdInfo2::GetDefaultAudioLanguage
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
 - IDvdInfo2::GetDefaultAudioLanguage
 - strmif/IDvdInfo2::GetDefaultAudioLanguage
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
 - IDvdInfo2.GetDefaultAudioLanguage
---

# IDvdInfo2::GetDefaultAudioLanguage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDefaultAudioLanguage</code> method retrieves the default audio language.

## -parameters

### -param pLanguage [out]

Receives the default language information.

### -param pAudioExtension

Pointer to a variable of type [DVD_AUDIO_LANG_EXT](/windows/desktop/api/strmif/ne-strmif-dvd_audio_lang_ext) that receives a value indicating the default DVD audio language extension.

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
The <i>pLanguage</i> parameter is <b>NULL</b>.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
DVD Navigator is not in a valid domain.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>