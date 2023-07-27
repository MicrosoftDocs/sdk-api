---
UID: NF:strmif.IDvdControl.BackwardScan
title: IDvdControl::BackwardScan (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Searches backward through the current disc at the specified speed.
helpviewer_keywords: ["BackwardScan","BackwardScan method [DirectShow]","BackwardScan method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","BackwardScan method","IDvdControl.BackwardScan","IDvdControl::BackwardScan","IDvdControlBackwardScan","dshow.idvdcontrol_backwardscan","strmif/IDvdControl::BackwardScan"]
old-location: dshow\idvdcontrol_backwardscan.htm
tech.root: dshow
ms.assetid: 9d2b1635-9b02-465a-a725-8b7985b651fb
ms.date: 4/26/2023
ms.keywords: BackwardScan, BackwardScan method [DirectShow], BackwardScan method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],BackwardScan method, IDvdControl.BackwardScan, IDvdControl::BackwardScan, IDvdControlBackwardScan, dshow.idvdcontrol_backwardscan, strmif/IDvdControl::BackwardScan
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
 - IDvdControl::BackwardScan
 - strmif/IDvdControl::BackwardScan
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
 - IDvdControl.BackwardScan
---

# IDvdControl::BackwardScan


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Searches backward through the current disc at the specified speed.

## -parameters

### -param dwSpeed [in]

Value that specifies how quickly DirectShow will search through the media file. This value is a multiplier, where 1.0 is the authored speed, so a value of 2.5 will search backward at two and one-half times the authored speed, while a value of 0.5 will search backward at half the authored speed. The actual speed of playback depends on the capabilities of the video decoder, and might differ from the specified rate.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>