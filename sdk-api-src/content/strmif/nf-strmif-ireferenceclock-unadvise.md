---
UID: NF:strmif.IReferenceClock.Unadvise
title: IReferenceClock::Unadvise (strmif.h)
description: The Unadvise method removes a pending advise request.
helpviewer_keywords: ["IReferenceClock interface [DirectShow]","Unadvise method","IReferenceClock.Unadvise","IReferenceClock::Unadvise","IReferenceClockUnadvise","Unadvise","Unadvise method [DirectShow]","Unadvise method [DirectShow]","IReferenceClock interface","dshow.ireferenceclock_unadvise","strmif/IReferenceClock::Unadvise"]
old-location: dshow\ireferenceclock_unadvise.htm
tech.root: dshow
ms.assetid: 1f032036-4502-473a-93e1-976a66d8bde1
ms.date: 4/26/2023
ms.keywords: IReferenceClock interface [DirectShow],Unadvise method, IReferenceClock.Unadvise, IReferenceClock::Unadvise, IReferenceClockUnadvise, Unadvise, Unadvise method [DirectShow], Unadvise method [DirectShow],IReferenceClock interface, dshow.ireferenceclock_unadvise, strmif/IReferenceClock::Unadvise
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IReferenceClock::Unadvise
 - strmif/IReferenceClock::Unadvise
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
 - IReferenceClock.Unadvise
---

# IReferenceClock::Unadvise


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Unadvise</code> method removes a pending advise request.

## -parameters

### -param dwAdviseCookie [in]

Identifier of the request to remove. Use the value returned by <a href="/windows/desktop/api/strmif/nf-strmif-ireferenceclock-advisetime">IReferenceClock::AdviseTime</a> or <a href="/windows/desktop/api/strmif/nf-strmif-ireferenceclock-adviseperiodic">IReferenceClock::AdvisePeriodic</a> in the <i>pdwAdviseToken</i> parameter.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Not found.

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock Interface</a>