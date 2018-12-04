---
UID: NF:strmif.IPinConnection.NotifyEndOfStream
title: IPinConnection::NotifyEndOfStream
author: windows-sdk-content
description: The NotifyEndOfStream method requests notification from the pin when the next end-of-stream condition occurs.
old-location: dshow\ipinconnection_notifyendofstream.htm
tech.root: DirectShow
ms.assetid: 3a911436-a679-4a86-93f9-e9c57ca762c5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPinConnection interface [DirectShow],NotifyEndOfStream method, IPinConnection.NotifyEndOfStream, IPinConnection::NotifyEndOfStream, IPinConnectionNotifyEndOfStream, NotifyEndOfStream, NotifyEndOfStream method [DirectShow], NotifyEndOfStream method [DirectShow],IPinConnection interface, dshow.ipinconnection_notifyendofstream, strmif/IPinConnection::NotifyEndOfStream
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
 - IPinConnection.NotifyEndOfStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPinConnection::NotifyEndOfStream


## -description



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
<li>It calls <a href="https://msdn.microsoft.com/b0cca250-9603-4d58-8af5-5b272730e5fa">IPin::EndOfStream</a> on the input pin connected to pin A.</li>
<li>As the remaining data travels downstream through any intermediate filters, those filters propagate the end-of-stream notification.</li>
<li>When pin B receives the end-of-stream notification, it signals the event given in the <i>hNotifyEvent</i> parameter. At that point, the caller can safely reconfigure the graph between pin A and pin B.</li>
</ol>
Because the purpose of this method is to enable the caller to rebuild the graph dynamically and then restart the connection, the end-of-stream notification does not represent the actual end of the stream. Therefore, pin B does not propagate the end-of-stream condition or signal EC_COMPLETE. This is an exception to the usual rules for data flow in the filter graph.

It is the caller's responsibility to cancel notification by calling this method again with a <b>NULL</b> event handle.

The filter graph calls this method inside the <a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">IGraphConfig::Reconnect</a> method. If an application or filter does any specialized dynamic reconfiguration to the graph (using the <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a> method), it might call this method first in order to push data through the portion of the graph that is being reconfigured.




## -see-also




<a href="https://msdn.microsoft.com/5b777f64-6b62-48dd-8eae-6603582a452a">Dynamic Reconnection</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection Interface</a>
 

 

