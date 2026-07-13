---
UID: NF:strmif.IDvdControl.ChapterPlayAutoStop
title: IDvdControl::ChapterPlayAutoStop (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Instructs the DVD player to start playing at the specified chapter within the specified title and play the number of chapters specified.
helpviewer_keywords: ["ChapterPlayAutoStop","ChapterPlayAutoStop method [DirectShow]","ChapterPlayAutoStop method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ChapterPlayAutoStop method","IDvdControl.ChapterPlayAutoStop","IDvdControl::ChapterPlayAutoStop","IDvdControlChapterPlayAutoStop","dshow.idvdcontrol_chapterplayautostop","strmif/IDvdControl::ChapterPlayAutoStop"]
old-location: dshow\idvdcontrol_chapterplayautostop.htm
tech.root: dshow
ms.assetid: 0c599647-c894-47b9-a62d-3ffd22843f7c
ms.date: 4/26/2023
ms.keywords: ChapterPlayAutoStop, ChapterPlayAutoStop method [DirectShow], ChapterPlayAutoStop method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterPlayAutoStop method, IDvdControl.ChapterPlayAutoStop, IDvdControl::ChapterPlayAutoStop, IDvdControlChapterPlayAutoStop, dshow.idvdcontrol_chapterplayautostop, strmif/IDvdControl::ChapterPlayAutoStop
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
 - IDvdControl::ChapterPlayAutoStop
 - strmif/IDvdControl::ChapterPlayAutoStop
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
 - IDvdControl.ChapterPlayAutoStop
---

# IDvdControl::ChapterPlayAutoStop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Instructs the DVD player to start playing at the specified chapter within the specified title and play the number of chapters specified.

## -parameters

### -param ulTitle [in]

Title number for playback.

### -param ulChapter [in]

Chapter number to start playback.

### -param ulChaptersToPlay [in]

Number of chapters to play from the start chapter.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is valid in any domain. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

Chapters range from 1 through 999. See EC_DVD_CHAPTER_AUTOSTOP in <a href="/windows/desktop/DirectShow/dvd-notification-codes">DVD Event Notification Codes</a> for more information.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>