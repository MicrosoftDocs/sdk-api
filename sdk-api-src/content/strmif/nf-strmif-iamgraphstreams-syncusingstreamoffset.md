---
UID: NF:strmif.IAMGraphStreams.SyncUsingStreamOffset
title: IAMGraphStreams::SyncUsingStreamOffset (strmif.h)
description: The SyncUsingStreamOffset method enables or disables synchronization using time-stamp offsets.
helpviewer_keywords: ["IAMGraphStreams interface [DirectShow]","SyncUsingStreamOffset method","IAMGraphStreams.SyncUsingStreamOffset","IAMGraphStreams::SyncUsingStreamOffset","IAMGraphStreamsSyncUsingStreamOffset","SyncUsingStreamOffset","SyncUsingStreamOffset method [DirectShow]","SyncUsingStreamOffset method [DirectShow]","IAMGraphStreams interface","dshow.iamgraphstreams_syncusingstreamoffset","strmif/IAMGraphStreams::SyncUsingStreamOffset"]
old-location: dshow\iamgraphstreams_syncusingstreamoffset.htm
tech.root: dshow
ms.assetid: 1a61da3a-3933-4543-b733-1b8a60929e43
ms.date: 4/26/2023
ms.keywords: IAMGraphStreams interface [DirectShow],SyncUsingStreamOffset method, IAMGraphStreams.SyncUsingStreamOffset, IAMGraphStreams::SyncUsingStreamOffset, IAMGraphStreamsSyncUsingStreamOffset, SyncUsingStreamOffset, SyncUsingStreamOffset method [DirectShow], SyncUsingStreamOffset method [DirectShow],IAMGraphStreams interface, dshow.iamgraphstreams_syncusingstreamoffset, strmif/IAMGraphStreams::SyncUsingStreamOffset
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
 - IAMGraphStreams::SyncUsingStreamOffset
 - strmif/IAMGraphStreams::SyncUsingStreamOffset
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
 - IAMGraphStreams.SyncUsingStreamOffset
---

# IAMGraphStreams::SyncUsingStreamOffset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SyncUsingStreamOffset</code> method enables or disables synchronization using time-stamp offsets.

## -parameters

### -param bUseStreamOffset [in]

Boolean value indicating whether to use a time-stamp offset. If <b>TRUE</b>, live sources will use a time-stamp offset to synchronize streams.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -remarks

By default, the filter graph does not attempt to synchronize live streams by means of time-stamp offsets. Call this method with a value of <b>TRUE</b> if you want the filter graph to determine the maximum latency in the graph and adjust time stamps accordingly. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-iampushsource-setstreamoffset">IAMPushSource::SetStreamOffset</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamgraphstreams">IAMGraphStreams Interface</a>