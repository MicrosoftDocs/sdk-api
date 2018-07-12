---
UID: NN:sbtsv.ITsSbProvider
title: ITsSbProvider
author: windows-sdk-content
description: Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.
old-location: termserv\itssbprovider.htm
old-project: TermServ
ms.assetid: a8574750-d86e-4b0d-a534-d005596e2a33
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ITsSbProvider, ITsSbProvider interface [Remote Desktop Services], ITsSbProvider interface [Remote Desktop Services],described, sbtsv/ITsSbProvider, termserv.itssbprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbProvider interface


## -description


Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.

The  <b>ITsSbProvider</b> interface is a helper interface, aimed at reducing the amount of code that the plug-in 
implementer needs to write. It provides a default implementation of some objects, such as 
environment, target, and session objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11570f40-979e-4caf-81af-f8d16ec61391">CreateEnvironmentObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> environment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52bb5c05-f8eb-42c9-862f-d42e71507a91">CreateEnvironmentPropertySetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a> environment property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaa13ec1-d79c-4458-9340-3cc42bbcd948">CreateLoadBalanceResultObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/f19f006c-e74a-4f44-8be8-f71852d4c305">ITsSbLoadBalanceResult</a> load-balancing result 
object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a15edb7a-4ff5-4832-8632-17b08cff4675">CreatePluginPropertySet</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a> plug-in property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14c800f8-a3d6-4d12-b568-94ef2d8e0aaf">CreateSessionObject</a>
</td>
<td align="left" width="63%">
Plug-ins can use the <a href="https://msdn.microsoft.com/14c800f8-a3d6-4d12-b568-94ef2d8e0aaf">CreateSessionObject</a> method to create an <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> session object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ee426a3-03fa-4535-84b6-f965bd9eba60">CreateTargetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82e9d414-2137-44f3-a984-dc12aba3ecd9">CreateTargetPropertySetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/74ea8132-cb06-40ce-b3bf-4bd8babe3711">ITsSbTargetPropertySet</a> target property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ba9d60-7dde-4aa1-b95e-ec26aef731ca">GetFilterPluginStore</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/59541fc2-0063-41ca-bcfe-536bb1742c6e">FilterPluginStore</a> instance of the  filter plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c83775-56e7-4342-a26a-418f472e190f">GetInstanceOfGlobalStore</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a> instance of the global store object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e4d5b1d-100e-49e1-b1b5-4b126683c329">GetResourcePluginStore</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a> instance of the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71e55a94-7e15-45f1-a1f3-d3cf8814e0c1">RegisterForNotification</a>
</td>
<td align="left" width="63%">
Requests that  RD Connection Broker send notifications about specified events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2fa297e-9923-4e60-9e6e-caa6e4b8c963">UnRegisterForNotification</a>
</td>
<td align="left" width="63%">
Requests that  RD Connection Broker not send notifications about specified events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

