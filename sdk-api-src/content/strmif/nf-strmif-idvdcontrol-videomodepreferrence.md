---
UID: NF:strmif.IDvdControl.VideoModePreferrence
title: IDvdControl::VideoModePreferrence (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the video display mode the user prefers.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","VideoModePreferrence method","IDvdControl.VideoModePreferrence","IDvdControl::VideoModePreferrence","IDvdControlVideoModePreferrence","VideoModePreferrence","VideoModePreferrence method [DirectShow]","VideoModePreferrence method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_videomodepreferrence","strmif/IDvdControl::VideoModePreferrence"]
old-location: dshow\idvdcontrol_videomodepreferrence.htm
tech.root: dshow
ms.assetid: 9e68b09c-534c-46d2-bda0-72f3d1d86b66
ms.date: 4/26/2023
ms.keywords: IDvdControl interface [DirectShow],VideoModePreferrence method, IDvdControl.VideoModePreferrence, IDvdControl::VideoModePreferrence, IDvdControlVideoModePreferrence, VideoModePreferrence, VideoModePreferrence method [DirectShow], VideoModePreferrence method [DirectShow],IDvdControl interface, dshow.idvdcontrol_videomodepreferrence, strmif/IDvdControl::VideoModePreferrence
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
 - IDvdControl::VideoModePreferrence
 - strmif/IDvdControl::VideoModePreferrence
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
 - IDvdControl.VideoModePreferrence
---

# IDvdControl::VideoModePreferrence


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the video display mode the user prefers.

## -parameters

### -param ulPreferredDisplayMode [in]

Value that specifies the new display mode for DVD content. Member of the [DVD_PREFERRED_DISPLAY_MODE](/windows/desktop/api/strmif/ne-strmif-dvd_preferred_display_mode) enumerated data type.

## -returns

Returns an <b>HRESULT</b> value .

## -remarks

This method changes the default video window's aspect ratio, and can also specify a default aspect ratio conversion mechanism.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>