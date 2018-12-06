---
UID: NN:mswmdm.ISCPSecureAuthenticate
title: ISCPSecureAuthenticate
author: windows-sdk-content
description: The ISCPSecureAuthenticate interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider.
old-location: wmdm\iscpsecureauthenticate.htm
tech.root: WMDM
ms.assetid: dfe37b41-f80b-4992-84c1-c23581cc4b69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISCPSecureAuthenticate, ISCPSecureAuthenticate interface [windows Media Device Manager], ISCPSecureAuthenticate interface [windows Media Device Manager],described, ISCPSecureAuthenticateInterface, mswmdm/ISCPSecureAuthenticate, wmdm.iscpsecureauthenticate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - ISCPSecureAuthenticate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureAuthenticate interface


## -description



The <b>ISCPSecureAuthenticate</b> interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider. This interface is used to pass information about the content to the secure content provider module, which the provider uses to report back whether it is responsible for the content. Windows Media Device Manager consults this interface whenever an application downloads content to a media device.

The secure content provider implements this interface, and Windows Media Device Manager calls its methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureAuthenticate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISCPSecureAuthenticate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureAuthenticate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0cee36c-5200-4951-9a83-a0f32658939b">GetSecureQuery</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

