---
UID: NN:wmsdkidl.IWMClientConnections
title: IWMClientConnections
author: windows-sdk-content
description: The IWMClientConnections interface manages the collecting of information about clients connected to a writer network sink object.The writer network sink object exposes this interface.
old-location: wmformat\iwmclientconnections.htm
tech.root: wmformat
ms.assetid: fea7cd85-22ab-4f3b-8a0a-301496f0c788
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMClientConnections, IWMClientConnections interface [windows Media Format], IWMClientConnections interface [windows Media Format],described, IWMClientConnectionsInterface, wmformat.iwmclientconnections, wmsdkidl/IWMClientConnections
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
 - IWMClientConnections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMClientConnections interface


## -description



The <b>IWMClientConnections</b> interface manages the collecting of information about clients connected to a writer network sink object.

The writer network sink object exposes this interface. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface on a writer network sink object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMClientConnections</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMClientConnections</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/208b40cd-c138-4311-8702-18a61713b71a">GetClientCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of connected clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a05d7d1e-21dc-4e2a-a17b-5f04e639b143">GetClientProperties</a>
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
<a href="https://msdn.microsoft.com/7148dd13-e5de-4adb-89e7-3f02a463c2d1">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3831b727-7fdc-4d05-a7b3-86ca5b5c3b17">IWMRegisterCallback</a>
</td>
<td>IID_IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink</a>
</td>
<td>IID_IWMWriterNetworkSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7148dd13-e5de-4adb-89e7-3f02a463c2d1">IWMClientConnections2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>
 

 

