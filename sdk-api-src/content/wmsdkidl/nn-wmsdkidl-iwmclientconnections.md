---
UID: NN:wmsdkidl.IWMClientConnections
title: IWMClientConnections (wmsdkidl.h)
description: The IWMClientConnections interface manages the collecting of information about clients connected to a writer network sink object.The writer network sink object exposes this interface.
helpviewer_keywords: ["IWMClientConnections","IWMClientConnections interface [windows Media Format]","IWMClientConnections interface [windows Media Format]","described","IWMClientConnectionsInterface","wmformat.iwmclientconnections","wmsdkidl/IWMClientConnections"]
old-location: wmformat\iwmclientconnections.htm
tech.root: wmformat
ms.assetid: fea7cd85-22ab-4f3b-8a0a-301496f0c788
ms.date: 12/05/2018
ms.keywords: IWMClientConnections, IWMClientConnections interface [windows Media Format], IWMClientConnections interface [windows Media Format],described, IWMClientConnectionsInterface, wmformat.iwmclientconnections, wmsdkidl/IWMClientConnections
f1_keywords:
- wmsdkidl/IWMClientConnections
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
- IWMClientConnections
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMClientConnections interface


## -description



The <b>IWMClientConnections</b> interface manages the collecting of information about clients connected to a writer network sink object.

The writer network sink object exposes this interface. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface on a writer network sink object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMClientConnections</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMClientConnections</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMClientConnections</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmclientconnections-getclientcount">GetClientCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of connected clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmclientconnections-getclientproperties">GetClientProperties</a>
</td>
<td align="left" width="63%">
Retrieves information, including the IP address and protocol, about a connected client.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback">IWMRegisterCallback</a>
</td>
<td>IID_IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink</a>
</td>
<td>IID_IWMWriterNetworkSink</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>
 

 

