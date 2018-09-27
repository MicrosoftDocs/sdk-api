---
UID: NF:strmif.IGraphConfig.Reconnect
title: IGraphConfig::Reconnect
author: windows-sdk-content
description: The Reconnect method performs a dynamic reconnection between two pins.
old-location: dshow\igraphconfig_reconnect.htm
tech.root: DirectShow
ms.assetid: e8cfac8e-df89-444d-bcc7-0cbc7ab5a592
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IGraphConfig interface [DirectShow],Reconnect method, IGraphConfig.Reconnect, IGraphConfig::Reconnect, IGraphConfigReconnect, Reconnect, Reconnect method [DirectShow], Reconnect method [DirectShow],IGraphConfig interface, dshow.igraphconfig_reconnect, strmif/IGraphConfig::Reconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfig::Reconnect


## -description



The <code>Reconnect</code> method performs a dynamic reconnection between two pins.




## -parameters




### -param pOutputPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of an output pin. Can be <b>NULL</b>, in which case <i>pInputPin</i> must not be <b>NULL</b>.


### -param pInputPin [in]

Pointer the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface to an input pin. Can be <b>NULL</b>, in which case <i>pOutputPin</i> must not be <b>NULL</b>.


### -param pmtFirstConnection [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type for the first pin connection made during the reconnection. If this parameter is <b>NULL</b>, the first connection can have any media type.


### -param pUsingFilter [in]

Pointer to an optional filter to use in the reconnection. The filter must already be in the graph. Can be <b>NULL</b>.


### -param hAbortEvent [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.


### -param dwFlags [in]

Combination of flags from the <a href="https://msdn.microsoft.com/59f47597-3270-48b3-b927-09b434373eac">AM_GRAPH_CONFIG_RECONNECT_FLAGS</a> enumeration, specifying how to perform the reconnection.


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
Input pin does not support <a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection</a>.

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



If you specify only one pin, the method will search for the other pin. By default, however, the search fails if it reaches a filter that was added to the graph by means of the <a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">IFilterGraph::AddFilter</a> method. To override this behavior, call <a href="https://msdn.microsoft.com/1f2ed50e-8bb9-4076-ad0e-a7311acb8285">IGraphConfig::SetFilterFlags</a> and set the AM_FILTER_FLAGS_REMOVABLE flag on the filter.

The reconnection process involves several steps, most of them handled inside this method:

<ol>
<li>First, before calling the method, make sure to block the flow of data along the path that is being reconfigured. Applications should call the <a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">IPinFlowControl::Block</a> method to do this. If the caller is a filter, rather than an application, possibly the filter can control the data flow internally.</li>
<li>The specified output and input pins define the starting and ending points for the reconnection. The input pin must support the <a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection</a> interface. If you leave one of these pins unspecified (by passing a <b>NULL</b> parameter), the method searches the filter graph to find a candidate pin for reconnection. (To find an input pin, it searches downstream from the output pin; to find an output pin, it searches upstream from the input pin.)</li>
<li>The method pushes any pending data through the filter graph (through an internal call to <a href="https://msdn.microsoft.com/f3d72a32-f43a-4a61-b25e-6d472aa629de">IGraphConfig::PushThroughData</a>).</li>
<li>If you have specified a filter to insert into the graph, the method connects the starting output pin to the filter's input pin, and connects the filter's output pin to the final input pin. If you do not specify a filter, the method simply connects the output pin to the input pin. In either case, the method inserts any transform filters required to complete the connections. (However, you can override this behavior by setting the appropriate flag; for more information see the description of the <i>dwFlags</i> parameter.)</li>
<li>Finally, the method places the new filters into a running state. It is up to the caller to restart the data flow. Applications can do this by calling <a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">IPinFlowControl::Block</a> with no flags.</li>
</ol>
If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="https://msdn.microsoft.com/8c415b5c-1aee-4ea4-b182-fd95da4898aa">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

