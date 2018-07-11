---
UID: NN:wmsdkidl.IWMWriterNetworkSink
title: IWMWriterNetworkSink
author: windows-sdk-content
description: The IWMWriterNetworkSink interface is used to deliver streams to the network.
old-location: wmformat\iwmwriternetworksink.htm
old-project: wmformat
ms.assetid: 3204c360-f407-4cf3-bb21-7e6094587fb0
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMWriterNetworkSink, IWMWriterNetworkSink interface [windows Media Format], IWMWriterNetworkSink interface [windows Media Format],described, IWMWriterNetworkSinkInterface, wmformat.iwmwriternetworksink, wmsdkidl/IWMWriterNetworkSink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterNetworkSink interface


## -description



The <b>IWMWriterNetworkSink</b> interface is used to deliver streams to the network. It inherits all the methods of <b>IWMWriterSink</b>, and adds methods to configure the network sink.

The network sink object exposes this interface. To create the network sink object, call the <a href="https://msdn.microsoft.com/5d391867-dece-4d40-80e2-99071d332984">WMCreateWriterNetworkSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterNetworkSink</b> interface inherits from <a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>. <b>IWMWriterNetworkSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink, and releases the port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf4f294c-148c-469f-83e7-c2cd1c585aa3">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects all clients from the network sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66d4747e-aec5-47bd-ac4a-dc052e964601">GetHostURL</a>
</td>
<td align="left" width="63%">
Retrieves URL from which the stream is broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0ef3fd6-aed7-40ec-96e6-7962e77bdd46">GetMaximumClients</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of clients that can connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5007b5be-9521-46f4-8e5c-85e70d48e99f">GetNetworkProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the network protocol that the network sink uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a network port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/619f0684-28bb-4412-acbf-27434672083a">SetMaximumClients</a>
</td>
<td align="left" width="63%">
Sets the maximum number of clients that connect to this sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ad6b2a4-b50b-45a0-8aa0-cabfc1e59bb7">SetNetworkProtocol</a>
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
<a href="https://msdn.microsoft.com/7251c600-90a2-4903-b26a-643b4d10b0ce">IWMAddressAccess</a>
</td>
<td>IID_IWMAddressAccess</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7148dd13-e5de-4adb-89e7-3f02a463c2d1">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1b04f361-8147-4f6a-8c9d-d8eeed28550a">Broadcasting ASF Data</a>



<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

