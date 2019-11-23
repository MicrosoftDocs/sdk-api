---
UID: NN:objidlbase.IRpcStubBuffer
title: IRpcStubBuffer (objidlbase.h)

description: Controls the RPC stub used to marshal data between COM components.
old-location: com\irpcstubbuffer.htm
tech.root: com
ms.assetid: 0aa724f0-6110-4ebf-a0c1-d309074a61d9

ms.date: 12/05/2018
ms.keywords: IRpcStubBuffer, IRpcStubBuffer interface [COM], IRpcStubBuffer interface [COM],described, _com_irpcstubbuffer, com.irpcstubbuffer, objidlbase/IRpcStubBuffer
ms.topic: interface
f1_keywords: 
 - "objidlbase/IRpcStubBuffer"
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
 - IRpcStubBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRpcStubBuffer interface


## -description


Controls the RPC stub used to marshal data between COM components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcStubBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRpcStubBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRpcStubBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-connect">Connect</a>
</td>
<td align="left" width="63%">
Initializes a server stub, binding it to the specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-countrefs">CountRefs</a>
</td>
<td align="left" width="63%">
Retrieves the total number of references that a stub has on the server object to which it is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-debugserverqueryinterface">DebugServerQueryInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the interface that a stub represents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-debugserverrelease">DebugServerRelease</a>
</td>
<td align="left" width="63%">
Releases an interface pointer that was previously returned by <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-debugserverqueryinterface">DebugServerQueryInterface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a server stub from any interface to which it is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Invokes the interface that a stub represents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-isiidsupported">IsIIDSupported</a>
</td>
<td align="left" width="63%">
Determines whether a stub is designed to handle the unmarshaling of a particular interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>
 

 

