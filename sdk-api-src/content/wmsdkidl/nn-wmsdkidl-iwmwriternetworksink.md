---
UID: NN:wmsdkidl.IWMWriterNetworkSink
title: IWMWriterNetworkSink (wmsdkidl.h)
description: The IWMWriterNetworkSink interface is used to deliver streams to the network.helpviewer_keywords: ["IWMWriterNetworkSink","IWMWriterNetworkSink interface [windows Media Format]","IWMWriterNetworkSink interface [windows Media Format]","described","IWMWriterNetworkSinkInterface","wmformat.iwmwriternetworksink","wmsdkidl/IWMWriterNetworkSink"]
old-location: wmformat\iwmwriternetworksink.htm
tech.root: wmformat
ms.assetid: 3204c360-f407-4cf3-bb21-7e6094587fb0
ms.date: 12/05/2018
ms.keywords: IWMWriterNetworkSink, IWMWriterNetworkSink interface [windows Media Format], IWMWriterNetworkSink interface [windows Media Format],described, IWMWriterNetworkSinkInterface, wmformat.iwmwriternetworksink, wmsdkidl/IWMWriterNetworkSink
f1_keywords:
- wmsdkidl/IWMWriterNetworkSink
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterNetworkSink interface


## -description



The <b>IWMWriterNetworkSink</b> interface is used to deliver streams to the network. It inherits all the methods of <b>IWMWriterSink</b>, and adds methods to configure the network sink.

The network sink object exposes this interface. To create the network sink object, call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink">WMCreateWriterNetworkSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterNetworkSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterNetworkSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close">Close</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink, and releases the port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl">GetHostURL</a>
</td>
<td align="left" width="63%">
Retrieves URL from which the stream is broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-getmaximumclients">GetMaximumClients</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of clients that can connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-getnetworkprotocol">GetNetworkProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the network protocol that the network sink uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open">Open</a>
</td>
<td align="left" width="63%">
Opens a network port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients">SetMaximumClients</a>
</td>
<td align="left" width="63%">
Sets the maximum number of clients that connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setnetworkprotocol">SetNetworkProtocol</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess</a>
</td>
<td>IID_IWMAddressAccess</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/broadcasting-asf-data">Broadcasting ASF Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

