---
UID: NF:control.IMediaControl.Run
title: IMediaControl::Run (control.h)
description: The Run method runs all the filters in the filter graph. While the graph is running, data moves through the graph and is rendered.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","Run method","IMediaControl.Run","IMediaControl::Run","IMediaControlRun","Run","Run method [DirectShow]","Run method [DirectShow]","IMediaControl interface","control/IMediaControl::Run","dshow.imediacontrol_run"]
old-location: dshow\imediacontrol_run.htm
tech.root: dshow
ms.assetid: b52a5fa7-96f8-4949-9cf0-2d526f23bee1
ms.date: 4/26/2023
ms.keywords: IMediaControl interface [DirectShow],Run method, IMediaControl.Run, IMediaControl::Run, IMediaControlRun, Run, Run method [DirectShow], Run method [DirectShow],IMediaControl interface, control/IMediaControl::Run, dshow.imediacontrol_run
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
 - IMediaControl::Run
 - control/IMediaControl::Run
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
 - IMediaControl.Run
---

# IMediaControl::Run


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Run</code> method runs all the filters in the filter graph. While the graph is running, data moves through the graph and is rendered.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The graph is preparing to run, but some filters have not completed the transition to a running state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
All filters in the graph completed the transition to a running state.

</td>
</tr>
</table>

## -remarks

If the filter graph is stopped, this method pauses the graph before running. If the graph is already running, the method returns S_OK but has no effect.

The graph runs until the application calls the <a href="/windows/desktop/api/control/nf-control-imediacontrol-pause">IMediaControl::Pause</a> or <a href="/windows/desktop/api/control/nf-control-imediacontrol-stop">IMediaControl::Stop</a> method. When playback reaches the end of the stream, the graph continues to run, but the filters do not stream any more data. At that point, the application can pause or stop the graph. For information about the end-of-stream event, see <b>IMediaControl::Pause</b> and <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a>.

This method does not seek to the beginning of the stream. Therefore, if you run the graph, pause it, and then run it again, playback resumes from the paused position. If you run the graph after it has reached the end of the stream, nothing is rendered. To seek the graph, use the <a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> interface.

If method returns <b>S_FALSE</b>, it means that the method returned before all of the filters switched to a running state. The filters will complete the transition after the method returns. Optionally, you can wait  for the transition to complete by calling the <a href="/windows/desktop/api/control/nf-control-imediacontrol-getstate">IMediaControl::GetState</a> method with a timeout value. However, this is not required.

If the <b>Run</b> method returns an error code, it means that one or more filters failed to run. However, some filters might be in a running state. In a multistream graph, entire streams might be playing successfully. Typically the application would tear down the graph and report an error in this case.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>
