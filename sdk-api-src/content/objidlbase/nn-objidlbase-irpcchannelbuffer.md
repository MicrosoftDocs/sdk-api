---
UID: NN:objidlbase.IRpcChannelBuffer
title: IRpcChannelBuffer (objidlbase.h)
author: windows-sdk-content
description: Marshals data between a COM client proxy and a COM server stub.
old-location: com\irpcchannelbuffer.htm
tech.root: com
ms.assetid: 1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRpcChannelBuffer, IRpcChannelBuffer interface [COM], IRpcChannelBuffer interface [COM],described, _com_irpcchannelbuffer, com.irpcchannelbuffer, objidlbase/IRpcChannelBuffer
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IRpcChannelBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRpcChannelBuffer interface


## -description


Marshals data between a COM client proxy and a COM server stub.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcChannelBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IRpcChannelBuffer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">GetBuffer</a>
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
 

 

