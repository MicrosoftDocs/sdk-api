---
UID: NF:strmif.IDvdControl.GoUp
title: IDvdControl::GoUp (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current media file and starts playback of the designated previous program chain (PGC).
helpviewer_keywords: ["GoUp","GoUp method [DirectShow]","GoUp method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","GoUp method","IDvdControl.GoUp","IDvdControl::GoUp","IDvdControlGoUp","dshow.idvdcontrol_goup","strmif/IDvdControl::GoUp"]
old-location: dshow\idvdcontrol_goup.htm
tech.root: dshow
ms.assetid: 2a553a5f-f221-4161-95f1-cb1629abb87a
ms.date: 4/26/2023
ms.keywords: GoUp, GoUp method [DirectShow], GoUp method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],GoUp method, IDvdControl.GoUp, IDvdControl::GoUp, IDvdControlGoUp, dshow.idvdcontrol_goup, strmif/IDvdControl::GoUp
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
 - IDvdControl::GoUp
 - strmif/IDvdControl::GoUp
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
 - IDvdControl.GoUp
---

# IDvdControl::GoUp


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current media file and starts playback of the designated previous program chain (PGC).



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Each PGC is associated with a previous PGC at authoring time, which this method sets as the new playback file.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
