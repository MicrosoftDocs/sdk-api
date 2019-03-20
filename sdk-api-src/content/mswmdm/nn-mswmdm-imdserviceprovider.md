---
UID: NN:mswmdm.IMDServiceProvider
title: IMDServiceProvider (mswmdm.h)
author: windows-sdk-content
description: The IMDServiceProvider interface is the initial interface that Windows Media Device Manager uses to connect to your service provider.
old-location: wmdm\imdserviceprovider.htm
tech.root: WMDM
ms.assetid: 803b6cc5-2cb2-42ad-a92c-05f098cbe8ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMDServiceProvider, IMDServiceProvider interface [windows Media Device Manager], IMDServiceProvider interface [windows Media Device Manager],described, IMDServiceProviderInterface, mswmdm/IMDServiceProvider, wmdm.imdserviceprovider
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
 - IMDServiceProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDServiceProvider interface


## -description



The <b>IMDServiceProvider</b> interface is the initial interface that Windows Media Device Manager uses to connect to your service provider. Using this interface, Windows Media Device Manager can enumerate and communicate with the all media devices supported by a particular service provider. The <a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2</a> interface can be implemented to create devices by using the device path.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDServiceProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDServiceProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDServiceProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3d4e404-7441-4a61-b2bb-ca373eb79b99">EnumDevices</a>
</td>
<td align="left" width="63%">
Enumerates the installed physical or software devices that are currently attached and are known by the service provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cca4cb7-f569-452f-92dc-409b996ede17">GetDeviceCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of media devices that are currently attached and are known by the service provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

