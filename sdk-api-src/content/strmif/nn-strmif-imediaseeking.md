---
UID: NN:strmif.IMediaSeeking
title: IMediaSeeking (strmif.h)
description: The IMediaSeeking interface contains methods for seeking to a position within a stream, and for setting the playback rate.
helpviewer_keywords: ["IMediaSeeking","IMediaSeeking interface [DirectShow]","IMediaSeeking interface [DirectShow]","described","IMediaSeekingInterface","dshow.imediaseeking","strmif/IMediaSeeking"]
old-location: dshow\imediaseeking.htm
tech.root: dshow
ms.assetid: 32adad53-d1ac-495f-9347-7bdd4ae4b78d
ms.date: 4/26/2023
ms.keywords: IMediaSeeking, IMediaSeeking interface [DirectShow], IMediaSeeking interface [DirectShow],described, IMediaSeekingInterface, dshow.imediaseeking, strmif/IMediaSeeking
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
 - IMediaSeeking
 - strmif/IMediaSeeking
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
 - IMediaSeeking
---

# IMediaSeeking interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaSeeking</code> interface contains methods for seeking to a position within a stream, and for setting the playback rate. The Filter Graph Manager exposes this interface, and so do individual filters or pins. Applications should query the Filter Graph Manager for the interface.

The Filter Graph Manager distributes any <code>IMediaSeeking</code> call to each of the renderer filters in the graph. The renderer filters send the call upstream to the source filters. This sequence of events ensures that all streams remain synchronized. If any of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received, even if some of the distributed calls succeed. An exception is E_NOTIMPL: the Filter Graph Manager does not return E_NOTIMPL unless it was returned by all of the distributed calls.

An application can seek the graph while the graph is in any state (running, paused or stopped). If the graph is running, the Filter Graph Manager pauses the graph before it issues the seek command. Then it runs the graph again. All seeking operations are independent of the current playback rate. Seeking operations cause any pending media data to be flushed from the graph.

For all <code>IMediaSeeking</code> parameters that specify time, the unit of time depends on the current time format. To set the time format, call the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method. Time formats are globally unique identifiers (GUIDs) defined in uuids.h. For more information, see <a href="/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.

## -inheritance

The <b>IMediaSeeking</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaSeeking</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/seeking-the-filter-graph">Seeking the Filter Graph</a>
