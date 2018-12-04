---
UID: NN:wmsdkidl.IWMWriterSink
title: IWMWriterSink
author: windows-sdk-content
description: The IWMWriterSink interface is the basic interface of all writer sinks, including the file, network, and push sinks defined in the Windows Media Format SDK, and custom sinks.
old-location: wmformat\iwmwritersink.htm
tech.root: wmformat
ms.assetid: 73656814-7fac-4567-abcd-dbb3243fcaa8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMWriterSink, IWMWriterSink interface [windows Media Format], IWMWriterSink interface [windows Media Format],described, IWMWriterSinkInterface, wmformat.iwmwritersink, wmsdkidl/IWMWriterSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterSink interface


## -description



The <b>IWMWriterSink</b> interface is the basic interface of all writer sinks, including the file, network, and push sinks defined in the Windows Media Format SDK, and custom sinks. If you are using one of the defined writer sinks, you never need to deal with the methods of this interface. If you are creating your own custom writer sink, you must implement these methods in your application.

This interface exists on the writer file sink object, the writer network sink object, and the writer push sink object. You should never obtain a pointer to this interface from one of these objects, however, as its methods are called internally by the writer sink objects and the writer object. You can create a class in your application that inherits from this interface to make your own sink.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMWriterSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56a16163-84e7-4235-8bf3-03e81696bb63">AllocateDataUnit</a>
</td>
<td align="left" width="63%">
Creates a buffer object to receive a data unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a32114-4581-4870-8c7f-b79b5af8f0a4">IsRealTime</a>
</td>
<td align="left" width="63%">
Ascertains whether the sink requires samples to be sent in real time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">OnDataUnit</a>
</td>
<td align="left" width="63%">
Called by the writer object when a data unit is ready for the sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5f653cc-e756-4f33-a6ce-3158e83129c8">OnEndWriting</a>
</td>
<td align="left" width="63%">
Called by the writer when all data units have been sent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b1dbd0-a555-40d3-b2f0-3a363a6ce168">OnHeader</a>
</td>
<td align="left" width="63%">
Called by the writer when the ASF header is ready for the sink.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/93f44579-fb2d-498e-a271-5bc91d6f0321">Writer File Sink Object</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>



<a href="https://msdn.microsoft.com/34e48f35-13d7-4649-a8b2-ed6510b16f88">Writer Push Sink Object</a>
 

 

