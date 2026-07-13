---
UID: NN:strmif.IAMAsyncReaderTimestampScaling
title: IAMAsyncReaderTimestampScaling (strmif.h)
description: Enables a pull-mode source filter to support larger file sizes.
helpviewer_keywords: ["IAMAsyncReaderTimestampScaling","IAMAsyncReaderTimestampScaling interface [DirectShow]","IAMAsyncReaderTimestampScaling interface [DirectShow]","described","dshow.iamasyncreadertimestampscaling","strmif/IAMAsyncReaderTimestampScaling"]
old-location: dshow\iamasyncreadertimestampscaling.htm
tech.root: dshow
ms.assetid: 159ed107-383d-4a1a-b172-f2e339d6bc83
ms.date: 4/26/2023
ms.keywords: IAMAsyncReaderTimestampScaling, IAMAsyncReaderTimestampScaling interface [DirectShow], IAMAsyncReaderTimestampScaling interface [DirectShow],described, dshow.iamasyncreadertimestampscaling, strmif/IAMAsyncReaderTimestampScaling
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAMAsyncReaderTimestampScaling
 - strmif/IAMAsyncReaderTimestampScaling
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
 - IAMAsyncReaderTimestampScaling
---

# IAMAsyncReaderTimestampScaling interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Enables a pull-mode source filter to support larger file sizes.

## -inheritance

The <b>IAMAsyncReaderTimestampScaling</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAsyncReaderTimestampScaling</b> also has these types of members:

## -remarks

In the pull model, the parser filter requests data from the source filter by calling <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a>. The input to this method is a media sample. The time stamp on the sample specifies the location to read in the stream, as a byte offset.

By default, the time stamp uses the following formula: Time = byte offset × 10000000. This scaling factor limits the effective file size to about 860 GB. To support larger file sizes, call <a href="/windows/desktop/api/strmif/nf-strmif-iamasyncreadertimestampscaling-settimestampmode">SetTimestampMode</a> with the value <b>TRUE</b>. This call sets the scaling factor to 1, so the formula becomes: Time = byte offset.

## -see-also

<a href="/windows/desktop/DirectShow/pull-model">Pull Model</a>
