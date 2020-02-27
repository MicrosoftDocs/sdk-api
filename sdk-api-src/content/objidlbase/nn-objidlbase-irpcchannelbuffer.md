---
UID: NN:objidlbase.IRpcChannelBuffer
title: IRpcChannelBuffer (objidlbase.h)
description: Marshals data between a COM client proxy and a COM server stub.
old-location: com\irpcchannelbuffer.htm
tech.root: com
ms.assetid: 1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20
ms.date: 12/05/2018
ms.keywords: IRpcChannelBuffer, IRpcChannelBuffer interface [COM], IRpcChannelBuffer interface [COM],described, _com_irpcchannelbuffer, com.irpcchannelbuffer, objidlbase/IRpcChannelBuffer
f1_keywords:
- objidlbase/IRpcChannelBuffer
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRpcChannelBuffer interface


## -description


Marshals data between a COM client proxy and a COM server stub.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcChannelBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRpcChannelBuffer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-freebuffer">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees a previously allocated RPC channel buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a buffer into which data can be marshaled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getdestctx">GetDestCtx</a>
</td>
<td align="left" width="63%">
Retrieves the destination context for the RPC channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-isconnected">IsConnected</a>
</td>
<td align="left" width="63%">
Determines whether the RPC channel is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-sendreceive">SendReceive</a>
</td>
<td align="left" width="63%">
Sends a method invocation across an RPC channel to the server stub.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
 

 

