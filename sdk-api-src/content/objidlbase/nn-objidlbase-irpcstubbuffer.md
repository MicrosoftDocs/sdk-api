---
UID: NN:objidlbase.IRpcStubBuffer
title: IRpcStubBuffer
author: windows-sdk-content
description: Controls the RPC stub used to marshal data between COM components.
old-location: com\irpcstubbuffer.htm
old-project: com
ms.assetid: 0aa724f0-6110-4ebf-a0c1-d309074a61d9
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IRpcStubBuffer, IRpcStubBuffer interface [COM], IRpcStubBuffer interface [COM],described, _com_irpcstubbuffer, com.irpcstubbuffer, objidlbase/IRpcStubBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IRpcStubBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRpcStubBuffer interface


## -description


Controls the RPC stub used to marshal data between COM components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcStubBuffer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRpcStubBuffer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0a452287-b674-4b51-9690-316beeab4482">Connect</a>
</td>
<td align="left" width="63%">
Initializes a server stub, binding it to the specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a2a629a-b935-47a2-a4c6-ba9f20641a03">CountRefs</a>
</td>
<td align="left" width="63%">
Retrieves the total number of references that a stub has on the server object to which it is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c735a99f-c67a-44eb-ae60-950dc4e68e74">DebugServerQueryInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the interface that a stub represents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/511f6e55-fb1d-4500-80fd-83e3fe2779d1">DebugServerRelease</a>
</td>
<td align="left" width="63%">
Releases an interface pointer that was previously returned by <a href="https://msdn.microsoft.com/c735a99f-c67a-44eb-ae60-950dc4e68e74">DebugServerQueryInterface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0ecd2b-a445-4ecb-a003-ef07fa1d0458">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a server stub from any interface to which it is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78d20830-78d7-4395-aaec-8a86b7c41cc7">Invoke</a>
</td>
<td align="left" width="63%">
Invokes the interface that a stub represents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7025d343-9171-4d0f-9e93-61365075edc0">IsIIDSupported</a>
</td>
<td align="left" width="63%">
Determines whether a stub is designed to handle the unmarshaling of a particular interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>



<a href="https://msdn.microsoft.com/e1b18997-f99b-4611-8ba6-da28fd8df898">IRpcProxyBuffer</a>
 

 

