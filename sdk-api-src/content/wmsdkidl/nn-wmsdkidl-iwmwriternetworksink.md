---
UID: NN:wmsdkidl.IWMWriterNetworkSink
title: IWMWriterNetworkSink
author: windows-sdk-content
description: The IWMWriterNetworkSink interface is used to deliver streams to the network.
old-location: wmformat\iwmwriternetworksink.htm
tech.root: wmformat
ms.assetid: 3204c360-f407-4cf3-bb21-7e6094587fb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterNetworkSink, IWMWriterNetworkSink interface [windows Media Format], IWMWriterNetworkSink interface [windows Media Format],described, IWMWriterNetworkSinkInterface, wmformat.iwmwriternetworksink, wmsdkidl/IWMWriterNetworkSink
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
 - IWMWriterNetworkSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterNetworkSink interface


## -description



The <b>IWMWriterNetworkSink</b> interface is used to deliver streams to the network. It inherits all the methods of <b>IWMWriterSink</b>, and adds methods to configure the network sink.

The network sink object exposes this interface. To create the network sink object, call the <a href="https://msdn.microsoft.com/en-us/library/Dd757791(v=VS.85).aspx">WMCreateWriterNetworkSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterNetworkSink</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>. <b>IWMWriterNetworkSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterNetworkSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798762(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink, and releases the port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798763(v=VS.85).aspx">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798764(v=VS.85).aspx">GetHostURL</a>
</td>
<td align="left" width="63%">
Retrieves URL from which the stream is broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798765(v=VS.85).aspx">GetMaximumClients</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of clients that can connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798766(v=VS.85).aspx">GetNetworkProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the network protocol that the network sink uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798767(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens a network port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798768(v=VS.85).aspx">SetMaximumClients</a>
</td>
<td align="left" width="63%">
Sets the maximum number of clients that connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798769(v=VS.85).aspx">SetNetworkProtocol</a>
</td>
<td align="left" width="63%">
Sets the network protocol that the network sink uses.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743279(v=VS.85).aspx">IWMAddressAccess</a>
</td>
<td>IID_IWMAddressAccess</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743303(v=VS.85).aspx">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743304(v=VS.85).aspx">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1b04f361-8147-4f6a-8c9d-d8eeed28550a">Broadcasting ASF Data</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

