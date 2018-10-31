---
UID: NN:objidlbase.IPSFactoryBuffer
title: IPSFactoryBuffer
author: windows-sdk-content
description: Provides custom methods for the creation of COM object proxies and stubs. This interface is not marshalable.
old-location: com\ipsfactorybuffer.htm
tech.root: com
ms.assetid: ffe85701-a4fa-4cf3-9b86-85f3a0cb63e9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPSFactoryBuffer, IPSFactoryBuffer interface [COM], IPSFactoryBuffer interface [COM],described, _com_ipsfactorybuffer, com.ipsfactorybuffer, objidlbase/IPSFactoryBuffer
ms.prod: windows
ms.technology: windows-sdk
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
 - IPSFactoryBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPSFactoryBuffer interface


## -description


Provides custom methods for the creation of COM object proxies and stubs. This interface is not marshalable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPSFactoryBuffer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPSFactoryBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPSFactoryBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d0638d9-50bc-47f3-8ebd-47bb5cbcab9c">CreateProxy</a>
</td>
<td align="left" width="63%">
Creates a proxy for the specified remote interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45e2a4c3-6a78-4018-9f32-ce5523682c0f">CreateStub</a>
</td>
<td align="left" width="63%">
Creates a stub for the remote use of the specified interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/6c82f655-ac46-4ed9-992b-0387b324a8f9">Proxy</a>



<a href="https://msdn.microsoft.com/ed7d5546-2d19-4055-b078-62b39d0317b7">Stub</a>
 

 

