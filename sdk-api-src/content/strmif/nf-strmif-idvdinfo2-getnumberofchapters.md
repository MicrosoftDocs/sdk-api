---
UID: NF:strmif.IDvdInfo2.GetNumberOfChapters
title: IDvdInfo2::GetNumberOfChapters (strmif.h)
description: The GetNumberOfChapters method retrieves the number of chapters in a given title.
helpviewer_keywords: ["GetNumberOfChapters","GetNumberOfChapters method [DirectShow]","GetNumberOfChapters method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetNumberOfChapters method","IDvdInfo2.GetNumberOfChapters","IDvdInfo2::GetNumberOfChapters","IDvdInfo2GetNumberOfChapters","dshow.idvdinfo2_getnumberofchapters","strmif/IDvdInfo2::GetNumberOfChapters"]
old-location: dshow\idvdinfo2_getnumberofchapters.htm
tech.root: dshow
ms.assetid: 5899fa87-56e2-4287-9325-1d9eaedb892b
ms.date: 4/26/2023
ms.keywords: GetNumberOfChapters, GetNumberOfChapters method [DirectShow], GetNumberOfChapters method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetNumberOfChapters method, IDvdInfo2.GetNumberOfChapters, IDvdInfo2::GetNumberOfChapters, IDvdInfo2GetNumberOfChapters, dshow.idvdinfo2_getnumberofchapters, strmif/IDvdInfo2::GetNumberOfChapters
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
 - IDvdInfo2::GetNumberOfChapters
 - strmif/IDvdInfo2::GetNumberOfChapters
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
 - IDvdInfo2.GetNumberOfChapters
---

# IDvdInfo2::GetNumberOfChapters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNumberOfChapters</code> method retrieves the number of chapters in a given title.

## -parameters

### -param ulTitle [in]

Specifies the title.

### -param pulNumOfChapters [out]

Receives the number of chapters for the specified title.

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
A parameter is invalid.

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
</table>

## -remarks

Call this method to get the number of chapters before calling <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchapter">IDvdControl2::PlayChapter</a>, to ensure that you specify a valid chapter number.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>