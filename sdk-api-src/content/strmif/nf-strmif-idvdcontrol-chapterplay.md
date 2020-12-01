---
UID: NF:strmif.IDvdControl.ChapterPlay
title: IDvdControl::ChapterPlay (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Plays the media file with the specified title index and chapter value.
helpviewer_keywords: ["ChapterPlay","ChapterPlay method [DirectShow]","ChapterPlay method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ChapterPlay method","IDvdControl.ChapterPlay","IDvdControl::ChapterPlay","IDvdControlChapterPlay","dshow.idvdcontrol_chapterplay","strmif/IDvdControl::ChapterPlay"]
old-location: dshow\idvdcontrol_chapterplay.htm
tech.root: dshow
ms.assetid: c51524d0-5935-4e14-bcaf-4739fd0f21bb
ms.date: 12/05/2018
ms.keywords: ChapterPlay, ChapterPlay method [DirectShow], ChapterPlay method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterPlay method, IDvdControl.ChapterPlay, IDvdControl::ChapterPlay, IDvdControlChapterPlay, dshow.idvdcontrol_chapterplay, strmif/IDvdControl::ChapterPlay
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
 - IDvdControl::ChapterPlay
 - strmif/IDvdControl::ChapterPlay
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
 - IDvdControl.ChapterPlay
---

# IDvdControl::ChapterPlay


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Plays the media file with the specified title index and chapter value.

## -parameters

### -param ulTitle [in]

Value that specifies the title number DirectShow will play back; this value must be from 1 through 99.

### -param ulChapter [in]

Value that specifies the chapter within the specified title where DirectShow will start playback; this value must be from 1 through 999.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>