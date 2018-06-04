---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRpcChannelBuffer interface


## -description


Marshals data between a COM client proxy and a COM server stub.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcChannelBuffer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRpcChannelBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRpcChannelBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcdd4783-4a75-42d0-86a9-ab2605abbbe1">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees a previously allocated RPC channel buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a buffer into which data can be marshaled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34599869-0c85-403a-88c2-ea8e865d533a">GetDestCtx</a>
</td>
<td align="left" width="63%">
Retrieves the destination context for the RPC channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4068f0bb-35fb-452b-8ab1-1a38b1a0c2fa">IsConnected</a>
</td>
<td align="left" width="63%">
Determines whether the RPC channel is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a42fd06-252f-4c1b-bbdb-abc2e3887c46">SendReceive</a>
</td>
<td align="left" width="63%">
Sends a method invocation across an RPC channel to the server stub.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/e1b18997-f99b-4611-8ba6-da28fd8df898">IRpcProxyBuffer</a>



<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>
 

 

