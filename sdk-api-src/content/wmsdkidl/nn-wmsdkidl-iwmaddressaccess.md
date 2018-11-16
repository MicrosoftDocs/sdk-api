---
UID: NN:wmsdkidl.IWMAddressAccess
title: IWMAddressAccess
author: windows-sdk-content
description: The IWMAddressAccess interface controls IP access lists on the writer network sink object.
old-location: wmformat\iwmaddressaccess.htm
tech.root: wmformat
ms.assetid: 7251c600-90a2-4903-b26a-643b4d10b0ce
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMAddressAccess, IWMAddressAccess interface [windows Media Format], IWMAddressAccess interface [windows Media Format],described, IWMAddressAccessInterface, wmformat.iwmaddressaccess, wmsdkidl/IWMAddressAccess
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
 - IWMAddressAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMAddressAccess interface


## -description



The <b>IWMAddressAccess</b> interface controls IP access lists on the writer network sink object. Applications can use this interface to exclude specific IP addresses, or ranges of IP addresses, from connecting to the network sink. To obtain this interface, call <b>QueryInterface</b> on another interface of the writer network sink object.

This interface supports only Internet Protocol version 4 (IPv4) addresses. The <a href="https://msdn.microsoft.com/609a20a7-e1a3-4889-abf3-4a6defc7739a">IWMAddressAccess2</a> interface inherits <b>IWMAddressAccess</b> and adds support for IPv6 addresses.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/609a20a7-e1a3-4889-abf3-4a6defc7739a">IWMAddressAccess2</a>
</td>
<td> IID_IWMAddressAccess2 </td>
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
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMAddressAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMAddressAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMAddressAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/670bea6a-0370-4dc4-a2af-fcdbe2a6656a">AddAccessEntry</a>
</td>
<td align="left" width="63%">
Adds an entry to the access list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b01b921b-0bb8-447b-877c-8ac218422d36">GetAccessEntry</a>
</td>
<td align="left" width="63%">
Retrieves an entry from the access list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/996d8a8a-887e-4e2f-b810-c57a4251f771">GetAccessEntryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the access list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3f9d493-90b4-4b2a-ad18-baf2b09bc72e">RemoveAccessEntry</a>
</td>
<td align="left" width="63%">
Removes an entry from the access list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>
 

 

