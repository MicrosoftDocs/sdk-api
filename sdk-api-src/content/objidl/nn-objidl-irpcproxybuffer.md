---
UID: NN:objidl.IRpcProxyBuffer
title: IRpcProxyBuffer (objidl.h)
description: Controls the RPC proxy used to marshal data between COM components.
old-location: com\irpcproxybuffer.htm
tech.root: com
ms.assetid: e1b18997-f99b-4611-8ba6-da28fd8df898
ms.date: 12/05/2018
ms.keywords: IRpcProxyBuffer, IRpcProxyBuffer interface [COM], IRpcProxyBuffer interface [COM],described, _com_irpcproxybuffer, com.irpcproxybuffer, objidlbase/IRpcProxyBuffer
ms.topic: interface
f1_keywords:
- objidl/IRpcProxyBuffer
dev_langs:
- c++
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- IRpcProxyBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRpcProxyBuffer interface


## -description


Controls the RPC proxy used to marshal data between COM components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcProxyBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRpcProxyBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRpcProxyBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcproxybuffer-connect">Connect</a>
</td>
<td align="left" width="63%">
Initializes a client proxy, binding it to the specified RPC channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcproxybuffer-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a client proxy from any RPC channel to which it is connected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
 

 

