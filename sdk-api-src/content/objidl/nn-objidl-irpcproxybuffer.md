---
UID: NN:objidl.IRpcProxyBuffer
title: IRpcProxyBuffer
author: windows-sdk-content
description: Controls the RPC proxy used to marshal data between COM components.
old-location: com\irpcproxybuffer.htm
old-project: com
ms.assetid: e1b18997-f99b-4611-8ba6-da28fd8df898
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IRpcProxyBuffer, IRpcProxyBuffer interface [COM], IRpcProxyBuffer interface [COM],described, _com_irpcproxybuffer, com.irpcproxybuffer, objidlbase/IRpcProxyBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IRpcProxyBuffer
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRpcProxyBuffer interface


## -description


Controls the RPC proxy used to marshal data between COM components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcProxyBuffer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRpcProxyBuffer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/18651110-9d20-4acc-b21e-9a93099e31bd">Connect</a>
</td>
<td align="left" width="63%">
Initializes a client proxy, binding it to the specified RPC channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ead4a47-7089-472d-b489-b725329ea5ab">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a client proxy from any RPC channel to which it is connected.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>



<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>
 

 

