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

# IComponentAuthenticate interface


## -description



The <b>IComponentAuthenticate</b> interface provides secure, encrypted communication between modules of Windows Media Device Manager. It is implemented by a service provider and created and used by an application or plug-in. To get this interface, the application calls <b>CoCreateInstance</b> (__uuidof(MediaDevMgr)).

The application creates and passes this interface to <a href="https://msdn.microsoft.com/b1af8f10-7bad-4f85-89f1-b983af6d4dc9">CSecureChannelClient::SetInterface</a>, but never calls any methods on this interface.

The service provider implements the methods in this interface, and calls them on a private <a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer</a> member.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentAuthenticate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComponentAuthenticate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponentAuthenticate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26cecd09-5f28-47e5-92ec-c2f277be8052">SACAuth</a>
</td>
<td align="left" width="63%">
Establishes a secure authenticated channel between components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db01f2a4-5cd5-4acc-be17-37b4c9861cc9">SACGetProtocols</a>
</td>
<td align="left" width="63%">
Discovers the authentication protocols supported by another component.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/011815fa-d55c-4abc-9ec8-55d754827342">Authenticating the Application</a>



<a href="https://msdn.microsoft.com/e48a8a7c-0277-4f0c-bad2-5bc9d0286da8">Authenticating the Service Provider</a>



<a href="https://msdn.microsoft.com/2d1abf2b-29d0-49b0-ae79-f07a35c42265">Interfaces for Service Providers and Applications</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

