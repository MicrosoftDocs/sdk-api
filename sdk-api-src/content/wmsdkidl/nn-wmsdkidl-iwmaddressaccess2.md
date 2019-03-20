---
UID: NN:wmsdkidl.IWMAddressAccess2
title: IWMAddressAccess2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMAddressAccess2 interface controls IP access lists on the writer network sink object.
old-location: wmformat\iwmaddressaccess2.htm
tech.root: wmformat
ms.assetid: 609a20a7-e1a3-4889-abf3-4a6defc7739a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMAddressAccess2, IWMAddressAccess2 interface [windows Media Format], IWMAddressAccess2 interface [windows Media Format],described, IWMAddressAccess2Interface, wmformat.iwmaddressaccess2, wmsdkidl/IWMAddressAccess2
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
 - IWMAddressAccess2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMAddressAccess2 interface


## -description



The <b>IWMAddressAccess2</b> interface controls IP access lists on the writer network sink object. Applications can use this interface to exclude specific IP addresses, or ranges of IP addresses, from connecting to the network sink. To obtain this interface, call <b>QueryInterface</b> on another interface of the writer network sink object.

This interface extends the <b>IWMAddressAccess</b> interface by adding support for Internet Protocol version 6 (IPv6) addresses.



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
<td> IID_IWMAddressAccess </td>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798761(v=VS.85).aspx">IWMWriterNetworkSink</a>
</td>
<td>IID_IWMWriterNetworkSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMAddressAccess2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743279(v=VS.85).aspx">IWMAddressAccess</a>. <b>IWMAddressAccess2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMAddressAccess2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743281(v=VS.85).aspx">AddAccessEntryEx</a>
</td>
<td align="left" width="63%">
Adds an entry to the access list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743282(v=VS.85).aspx">GetAccessEntryEx</a>
</td>
<td align="left" width="63%">
Retrieves an entry from the access list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743279(v=VS.85).aspx">IWMAddressAccess</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>
 

 

