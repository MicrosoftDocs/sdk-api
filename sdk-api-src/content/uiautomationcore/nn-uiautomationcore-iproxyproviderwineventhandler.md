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

# IProxyProviderWinEventHandler interface


## -description


Exposes a method that is implemented by proxy providers to handle WinEvents. To implement Microsoft UI Automation event handling, a proxy provider may need to handle WinEvents that are raised by the proxied UI. UI Automation will use the <b>IProxyProviderWinEventHandler</b> interface to notify the provider that a WinEvent has been raised for the provider window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProxyProviderWinEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProxyProviderWinEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProxyProviderWinEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a63cb9-3eae-43ec-aba1-2f038ca0896f">RespondToWinEvent</a>
</td>
<td align="left" width="63%">
Handles a WinEvent.

</td>
</tr>
</table> 

