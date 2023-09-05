---
UID: NF:strmif.IDvdInfo2.GetDVDTextNumberOfLanguages
title: IDvdInfo2::GetDVDTextNumberOfLanguages (strmif.h)
description: The GetDVDTextNumberOfLanguages method retrieves the number of languages in which DVD text strings appear.
helpviewer_keywords: ["GetDVDTextNumberOfLanguages","GetDVDTextNumberOfLanguages method [DirectShow]","GetDVDTextNumberOfLanguages method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDTextNumberOfLanguages method","IDvdInfo2.GetDVDTextNumberOfLanguages","IDvdInfo2::GetDVDTextNumberOfLanguages","IDvdInfo2GetDVDTextNumberOfLanguages","dshow.idvdinfo2_getdvdtextnumberoflanguages","strmif/IDvdInfo2::GetDVDTextNumberOfLanguages"]
old-location: dshow\idvdinfo2_getdvdtextnumberoflanguages.htm
tech.root: dshow
ms.assetid: 20c6ee1f-f20b-40c5-bc84-5ec1c07c0681
ms.date: 4/26/2023
ms.keywords: GetDVDTextNumberOfLanguages, GetDVDTextNumberOfLanguages method [DirectShow], GetDVDTextNumberOfLanguages method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextNumberOfLanguages method, IDvdInfo2.GetDVDTextNumberOfLanguages, IDvdInfo2::GetDVDTextNumberOfLanguages, IDvdInfo2GetDVDTextNumberOfLanguages, dshow.idvdinfo2_getdvdtextnumberoflanguages, strmif/IDvdInfo2::GetDVDTextNumberOfLanguages
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
 - IDvdInfo2::GetDVDTextNumberOfLanguages
 - strmif/IDvdInfo2::GetDVDTextNumberOfLanguages
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
 - IDvdInfo2.GetDVDTextNumberOfLanguages
---

# IDvdInfo2::GetDVDTextNumberOfLanguages


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDTextNumberOfLanguages</code> method retrieves the number of languages in which DVD text strings appear.

## -parameters

### -param pulNumOfLangs [out]

Receives the number of text languages.

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
An unexpected internal error occurred.

</td>
</tr>
</table>

## -remarks

Depending on how the disc is authored, the number of languages will be valid either for the entire disc, or only for the current side of the disc.

If the DVD does not contain any text strings, the method succeeds, but <i>pulNumOfLangs</i> receives the value zero.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>