---
UID: NF:control.IMediaControl.Stop
title: IMediaControl::Stop (control.h)
description: The Stop method stops all the filters in the graph.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","Stop method","IMediaControl.Stop","IMediaControl::Stop","IMediaControlStop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IMediaControl interface","control/IMediaControl::Stop","dshow.imediacontrol_stop"]
old-location: dshow\imediacontrol_stop.htm
tech.root: dshow
ms.assetid: 89e48d43-a31f-4912-98ff-36ba2069812d
ms.date: 4/26/2023
ms.keywords: IMediaControl interface [DirectShow],Stop method, IMediaControl.Stop, IMediaControl::Stop, IMediaControlStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IMediaControl interface, control/IMediaControl::Stop, dshow.imediacontrol_stop
req.header: control.h
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
 - IMediaControl::Stop
 - control/IMediaControl::Stop
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
 - IMediaControl.Stop
---

# IMediaControl::Stop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Stop</code> method stops all the filters in the graph.



## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value that indicates the cause of the error.

## -remarks

If the graph is running, this method pauses the graph before stopping it. While paused, video renderers can copy the current frame to display as a poster frame.

This method does not seek to the beginning of the stream. If you call this method and then call the <a href="/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a> method, playback resumes from the stopped position. To seek, use the <a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> interface.

The Filter Graph Manager pauses all the filters in the graph, and then calls the <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">IMediaFilter::Stop</a> method on all filters, without waiting for the pause operations to complete. Therefore, some filters might have their <code>Stop</code> method called before they complete their pause operation. If you develop a custom rendering filter, you might need to handle this case by pausing the filter if it receives a stop command while in a running state. However, most filters do not need to take any special action in this regard.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>



<a href="/windows/desktop/api/control/nf-control-imediacontrol-stopwhenready">StopWhenReady</a>
