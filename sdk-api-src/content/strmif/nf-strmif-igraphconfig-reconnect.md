---
UID: NF:strmif.IGraphConfig.Reconnect
title: IGraphConfig::Reconnect (strmif.h)
description: The Reconnect method performs a dynamic reconnection between two pins.
helpviewer_keywords: ["IGraphConfig interface [DirectShow]","Reconnect method","IGraphConfig.Reconnect","IGraphConfig::Reconnect","IGraphConfigReconnect","Reconnect","Reconnect method [DirectShow]","Reconnect method [DirectShow]","IGraphConfig interface","dshow.igraphconfig_reconnect","strmif/IGraphConfig::Reconnect"]
old-location: dshow\igraphconfig_reconnect.htm
tech.root: dshow
ms.assetid: e8cfac8e-df89-444d-bcc7-0cbc7ab5a592
ms.date: 4/26/2023
ms.keywords: IGraphConfig interface [DirectShow],Reconnect method, IGraphConfig.Reconnect, IGraphConfig::Reconnect, IGraphConfigReconnect, Reconnect, Reconnect method [DirectShow], Reconnect method [DirectShow],IGraphConfig interface, dshow.igraphconfig_reconnect, strmif/IGraphConfig::Reconnect
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
 - IGraphConfig::Reconnect
 - strmif/IGraphConfig::Reconnect
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
 - IGraphConfig.Reconnect
---

# IGraphConfig::Reconnect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reconnect</code> method performs a dynamic reconnection between two pins.

## -parameters

### -param pOutputPin [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of an output pin. Can be <b>NULL</b>, in which case <i>pInputPin</i> must not be <b>NULL</b>.

### -param pInputPin [in]

Pointer the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface to an input pin. Can be <b>NULL</b>, in which case <i>pOutputPin</i> must not be <b>NULL</b>.

### -param pmtFirstConnection [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type for the first pin connection made during the reconnection. If this parameter is <b>NULL</b>, the first connection can have any media type.

### -param pUsingFilter [in]

Pointer to an optional filter to use in the reconnection. The filter must already be in the graph. Can be <b>NULL</b>.

### -param hAbortEvent [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.

### -param dwFlags [in]

Combination of flags from the [AM_GRAPH_CONFIG_RECONNECT_FLAGS](/windows/desktop/api/strmif/ne-strmif-am_graph_config_reconnect_flags) enumeration, specifying how to perform the reconnection.

## -returns

Returns S_OK if successful. Otherwise, returns an error code that may be one of the following values, or others not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. (For example, both <i>pInputPin</i> and <i>pOutputPin</i> are <b>NULL</b>.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Input pin does not support <a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect filter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_STATE_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The state of the filter changed. Unable to complete the operation.

</td>
</tr>
</table>

## -remarks

If you specify only one pin, the method will search for the other pin. By default, however, the search fails if it reaches a filter that was added to the graph by means of the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">IFilterGraph::AddFilter</a> method. To override this behavior, call <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-setfilterflags">IGraphConfig::SetFilterFlags</a> and set the AM_FILTER_FLAGS_REMOVABLE flag on the filter.

The reconnection process involves several steps, most of them handled inside this method:

<ol>
<li>First, before calling the method, make sure to block the flow of data along the path that is being reconfigured. Applications should call the <a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a> method to do this. If the caller is a filter, rather than an application, possibly the filter can control the data flow internally.</li>
<li>The specified output and input pins define the starting and ending points for the reconnection. The input pin must support the <a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection</a> interface. If you leave one of these pins unspecified (by passing a <b>NULL</b> parameter), the method searches the filter graph to find a candidate pin for reconnection. (To find an input pin, it searches downstream from the output pin; to find an output pin, it searches upstream from the input pin.)</li>
<li>The method pushes any pending data through the filter graph (through an internal call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-pushthroughdata">IGraphConfig::PushThroughData</a>).</li>
<li>If you have specified a filter to insert into the graph, the method connects the starting output pin to the filter's input pin, and connects the filter's output pin to the final input pin. If you do not specify a filter, the method simply connects the output pin to the input pin. In either case, the method inserts any transform filters required to complete the connections. (However, you can override this behavior by setting the appropriate flag; for more information see the description of the <i>dwFlags</i> parameter.)</li>
<li>Finally, the method places the new filters into a running state. It is up to the caller to restart the data flow. Applications can do this by calling <a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a> with no flags.</li>
</ol>
If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>