---
UID: NF:strmif.IDvdControl.NextPGSearch
title: IDvdControl::NextPGSearch (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current program and starts playback from the next program within the program chain (PGC).
helpviewer_keywords: ["IDvdControl interface [DirectShow]","NextPGSearch method","IDvdControl.NextPGSearch","IDvdControl::NextPGSearch","IDvdControlNextPGSearch","NextPGSearch","NextPGSearch method [DirectShow]","NextPGSearch method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_nextpgsearch","strmif/IDvdControl::NextPGSearch"]
old-location: dshow\idvdcontrol_nextpgsearch.htm
tech.root: dshow
ms.assetid: a509f63f-a3e9-4b49-bbf0-f59051db119a
ms.date: 4/26/2023
ms.keywords: IDvdControl interface [DirectShow],NextPGSearch method, IDvdControl.NextPGSearch, IDvdControl::NextPGSearch, IDvdControlNextPGSearch, NextPGSearch, NextPGSearch method [DirectShow], NextPGSearch method [DirectShow],IDvdControl interface, dshow.idvdcontrol_nextpgsearch, strmif/IDvdControl::NextPGSearch
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
 - IDvdControl::NextPGSearch
 - strmif/IDvdControl::NextPGSearch
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
 - IDvdControl.NextPGSearch
---

# IDvdControl::NextPGSearch


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current program and starts playback from the next program within the program chain (PGC).



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

A program is usually equivalent to a chapter, and a PGC is usually equivalent to a title. In the case of One_Sequential_PGC_Titles, each program is required to be a chapter and each title has only one PGC, but in other cases (especially with random/shuffle PGCs and parental blocks) there can be more than one program between chapters and there can be more than one PGC in a title.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
