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

# ISearchProtocolThreadContext interface


## -description


This optional interface enables the protocol handler to perform an action on the thread used for filtering in the protocol host. When the protocol host starts, it first initializes all the protocol handlers, and then it creates the filtering thread(s). The methods on this interface enable protocol handlers to manage their resources that are used by a filtering thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocolThreadContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchProtocolThreadContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchProtocolThreadContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47e3c8e2-65aa-4e05-a8f6-5eace4cf35ea">ThreadIdle</a>
</td>
<td align="left" width="63%">
Notifies the protocol handler that the filtering thread is idle, so that the protocol handler can clean up any cache it might have built up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b68fa44-8fa1-401e-a089-af29bfa53e42">ThreadInit</a>
</td>
<td align="left" width="63%">
Initializes communication between the protocol handler and the protocol host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fb169da-ef5f-4930-b22c-d1197e79ab6e">ThreadShutdown</a>
</td>
<td align="left" width="63%">
Notifies the protocol handler that the thread is being shut down.

</td>
</tr>
</table> 

