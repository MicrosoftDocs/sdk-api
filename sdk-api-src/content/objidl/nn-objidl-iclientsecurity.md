---
UID: NN:objidl.IClientSecurity
title: IClientSecurity
author: windows-sdk-content
description: Gives the client control over the security settings for each individual interface proxy of an object.
old-location: com\iclientsecurity.htm
tech.root: com
ms.assetid: 65066913-f9d8-48c7-bcb5-68c8ddc4a009
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IClientSecurity, IClientSecurity interface [COM], IClientSecurity interface [COM],described, _com_iclientsecurity, com.iclientsecurity, objidl/IClientSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidl.h
req.include-header: 
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
 - ObjIdl.h
api_name:
 - IClientSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IClientSecurity interface


## -description


Gives the client control over the security settings for each individual interface proxy of an object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClientSecurity</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IClientSecurity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClientSecurity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4664351b-d43b-45dc-800e-574685afd0f6">CopyProxy</a>
</td>
<td align="left" width="63%">
Makes a private copy of the proxy for the specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8761bb58-9f28-4fe6-bf24-2687608ec5e8">QueryBlanket</a>
</td>
<td align="left" width="63%">
Retrieves authentication information the client uses to make calls on the specified proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">SetBlanket</a>
</td>
<td align="left" width="63%">
Sets the authentication information (the security blanket) that will be used to make calls on the specified proxy.

</td>
</tr>
</table> 


## -remarks



Every object has one proxy manager, and every proxy manager exposes the <b>IClientSecurity</b> interface automatically. Therefore, the client can query the proxy manager of an object for <b>IClientSecurity</b>, using any interface pointer on the object. If the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call succeeds, the <b>IClientSecurity</b> pointer can be used to call an <b>IClientSecurity</b> method, passing a pointer to the interface proxy that the client is interested in. If a call to <b>QueryInterface</b> for <b>IClientSecurity</b> fails, either the object is implemented in-process or it is remoted by a custom marshaler that does not support security. (A custom marshaler can support security by offering the <b>IClientSecurity</b> interface to the client.)

The interface proxies passed as parameters to <b>IClientSecurity</b> methods must be from the same object as the <b>IClientSecurity</b> interface. That is, each object has a distinct <b>IClientSecurity</b> interface; calling <b>IClientSecurity</b> on one object and passing a proxy to another object will not work. Also, you cannot pass an interface to an <b>IClientSecurity</b> method if the interface does not use a proxy. This means that interfaces implemented locally by the proxy manager cannot be passed to <b>IClientSecurity</b> methods, except for <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, which is the exception to this rule.




## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>



<a href="https://msdn.microsoft.com/20b66868-fb9a-489f-97a2-59a8a825c8d9">Setting Process-Wide Security with CoInitializeSecurity</a>
 

 

