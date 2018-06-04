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

# IMessageDispatcher interface


## -description


Callback interface implemented by components that need to perform special processing of window messages on an ASTA thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageDispatcher</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IMessageDispatcher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageDispatcher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC34B3B0-C956-4B37-8DF7-CC90A0160835">PumpMessages</a>
</td>
<td align="left" width="63%">
Performs custom dispatching when window messages are available to be dispatched on an ASTA thread.

</td>
</tr>
</table> 

