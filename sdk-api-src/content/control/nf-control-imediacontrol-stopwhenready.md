---
UID: NF:control.IMediaControl.StopWhenReady
title: IMediaControl::StopWhenReady (control.h)
description: The StopWhenReady method pauses the filter graph, allowing filters to queue data, and then stops the filter graph.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","StopWhenReady method","IMediaControl.StopWhenReady","IMediaControl::StopWhenReady","IMediaControlStopWhenReady","StopWhenReady","StopWhenReady method [DirectShow]","StopWhenReady method [DirectShow]","IMediaControl interface","control/IMediaControl::StopWhenReady","dshow.imediacontrol_stopwhenready"]
old-location: dshow\imediacontrol_stopwhenready.htm
tech.root: dshow
ms.assetid: 55dd55b1-51f0-4b47-8432-99741eaee8bb
ms.date: 4/26/2023
ms.keywords: IMediaControl interface [DirectShow],StopWhenReady method, IMediaControl.StopWhenReady, IMediaControl::StopWhenReady, IMediaControlStopWhenReady, StopWhenReady, StopWhenReady method [DirectShow], StopWhenReady method [DirectShow],IMediaControl interface, control/IMediaControl::StopWhenReady, dshow.imediacontrol_stopwhenready
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
 - IMediaControl::StopWhenReady
 - control/IMediaControl::StopWhenReady
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
 - IMediaControl.StopWhenReady
---

# IMediaControl::StopWhenReady


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StopWhenReady</code> method pauses the filter graph, allowing filters to queue data, and then stops the filter graph.



## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The graph was still transitioning to the paused state when the method returned.

</td>
</tr>
</table>

## -remarks

This method is useful if you want to seek the filter graph while the graph is stopped. As long as the filter graph is stopped, changes in the current position do not repaint the video window with a new frame. Therefore, calling <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-setpositions">IMediaSeeking::SetPositions</a> does not update the video window. To update the window after the seek operation, call <code>StopWhenReady</code>. This method transitions the graph to a paused state, waits for the pause operation to complete, and then transitions the graph back to stopped. The pause operation queues data in the graph, so that the video renderer receives and displays the new frame.

This method is asynchronous. It waits on a separate thread for the pause to complete. The calling thread does not block, which enables the application to respond to user input. When the method returns, the logical state of the graph is stopped, even before the pause operation completes. If you call the <a href="/windows/desktop/api/control/nf-control-imediacontrol-getstate">IMediaControl::GetState</a> method at this point, it returns State_Stopped.

If the application issues another state-change command (such as pause, run, or seek) before the pause operation completes, the new command cancels the pending stop command. The pause operation completes, but the graph does not stop.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>
