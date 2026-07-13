---
UID: NF:strmif.IDvdControl.ChapterSearch
title: IDvdControl::ChapterSearch (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current chapter and starts playback from the specified chapter within the same title.
helpviewer_keywords: ["ChapterSearch","ChapterSearch method [DirectShow]","ChapterSearch method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ChapterSearch method","IDvdControl.ChapterSearch","IDvdControl::ChapterSearch","IDvdControlChapterSearch","dshow.idvdcontrol_chaptersearch","strmif/IDvdControl::ChapterSearch"]
old-location: dshow\idvdcontrol_chaptersearch.htm
tech.root: dshow
ms.assetid: 1389df65-e269-4c2b-b276-a29da33fe515
ms.date: 4/26/2023
ms.keywords: ChapterSearch, ChapterSearch method [DirectShow], ChapterSearch method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterSearch method, IDvdControl.ChapterSearch, IDvdControl::ChapterSearch, IDvdControlChapterSearch, dshow.idvdcontrol_chaptersearch, strmif/IDvdControl::ChapterSearch
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
 - IDvdControl::ChapterSearch
 - strmif/IDvdControl::ChapterSearch
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
 - IDvdControl.ChapterSearch
---

# IDvdControl::ChapterSearch


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current chapter and starts playback from the specified chapter within the same title.

## -parameters

### -param ulChapter

Chapter value that specifies the point where playback will begin.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>