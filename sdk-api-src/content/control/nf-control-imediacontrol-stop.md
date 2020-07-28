---
UID: NF:control.IMediaControl.Stop
title: IMediaControl::Stop (control.h)
description: The Stop method stops all the filters in the graph.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","Stop method","IMediaControl.Stop","IMediaControl::Stop","IMediaControlStop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IMediaControl interface","control/IMediaControl::Stop","dshow.imediacontrol_stop"]
old-location: dshow\imediacontrol_stop.htm
tech.root: dshow
ms.assetid: 89e48d43-a31f-4912-98ff-36ba2069812d
ms.date: 12/05/2018
ms.keywords: IMediaControl interface [DirectShow],Stop method, IMediaControl.Stop, IMediaControl::Stop, IMediaControlStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IMediaControl interface, control/IMediaControl::Stop, dshow.imediacontrol_stop
f1_keywords:
- control/IMediaControl.Stop
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaControl::Stop


## -description



The <code>Stop</code> method stops all the filters in the graph.




## -parameters






## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value that indicates the cause of the error.




## -remarks



If the graph is running, this method pauses the graph before stopping it. While paused, video renderers can copy the current frame to display as a poster frame.

This method does not seek to the beginning of the stream. If you call this method and then call the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a> method, playback resumes from the stopped position. To seek, use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> interface.

The Filter Graph Manager pauses all the filters in the graph, and then calls the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">IMediaFilter::Stop</a> method on all filters, without waiting for the pause operations to complete. Therefore, some filters might have their <code>Stop</code> method called before they complete their pause operation. If you develop a custom rendering filter, you might need to handle this case by pausing the filter if it receives a stop command while in a running state. However, most filters do not need to take any special action in this regard.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-stopwhenready">StopWhenReady</a>
 

 

