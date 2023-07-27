---
UID: NF:strmif.IPinConnection.NotifyEndOfStream
title: IPinConnection::NotifyEndOfStream (strmif.h)
description: The NotifyEndOfStream method requests notification from the pin when the next end-of-stream condition occurs.
helpviewer_keywords: ["IPinConnection interface [DirectShow]","NotifyEndOfStream method","IPinConnection.NotifyEndOfStream","IPinConnection::NotifyEndOfStream","IPinConnectionNotifyEndOfStream","NotifyEndOfStream","NotifyEndOfStream method [DirectShow]","NotifyEndOfStream method [DirectShow]","IPinConnection interface","dshow.ipinconnection_notifyendofstream","strmif/IPinConnection::NotifyEndOfStream"]
old-location: dshow\ipinconnection_notifyendofstream.htm
tech.root: dshow
ms.assetid: 3a911436-a679-4a86-93f9-e9c57ca762c5
ms.date: 4/26/2023
ms.keywords: IPinConnection interface [DirectShow],NotifyEndOfStream method, IPinConnection.NotifyEndOfStream, IPinConnection::NotifyEndOfStream, IPinConnectionNotifyEndOfStream, NotifyEndOfStream, NotifyEndOfStream method [DirectShow], NotifyEndOfStream method [DirectShow],IPinConnection interface, dshow.ipinconnection_notifyendofstream, strmif/IPinConnection::NotifyEndOfStream
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
 - IPinConnection::NotifyEndOfStream
 - strmif/IPinConnection::NotifyEndOfStream
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
 - IPinConnection.NotifyEndOfStream
---

# IPinConnection::NotifyEndOfStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyEndOfStream</code> method requests notification from the pin when the next end-of-stream condition occurs.

## -parameters

### -param hNotifyEvent [in]

Handle to an event object that the pin will signal.

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
Event handle was <b>NULL</b>, but there was no existing event handle to reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Event handle was set. (If event handle was <b>NULL</b>, event notification was canceled.)

</td>
</tr>
</table>

## -remarks

This method enables the caller to push data through a portion of the filter graph ending with this pin.

For example, suppose the caller is pushing data from an output pin called "A" on one filter, to an input pin called "B" on another filter, possibly with intermediate filters connecting them. The following sequence of events would take place.

<ol>
<li>The caller blocks the data flow at pin A.</li>
<li>It calls <code>NotifyEndOfStream</code> on pin B.</li>
<li>It calls <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endofstream">IPin::EndOfStream</a> on the input pin connected to pin A.</li>
<li>As the remaining data travels downstream through any intermediate filters, those filters propagate the end-of-stream notification.</li>
<li>When pin B receives the end-of-stream notification, it signals the event given in the <i>hNotifyEvent</i> parameter. At that point, the caller can safely reconfigure the graph between pin A and pin B.</li>
</ol>
Because the purpose of this method is to enable the caller to rebuild the graph dynamically and then restart the connection, the end-of-stream notification does not represent the actual end of the stream. Therefore, pin B does not propagate the end-of-stream condition or signal EC_COMPLETE. This is an exception to the usual rules for data flow in the filter graph.

It is the caller's responsibility to cancel notification by calling this method again with a <b>NULL</b> event handle.

The filter graph calls this method inside the <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a> method. If an application or filter does any specialized dynamic reconfiguration to the graph (using the <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a> method), it might call this method first in order to push data through the portion of the graph that is being reconfigured.

## -see-also

<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection Interface</a>