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

# IOfflineFilesEventsFilter interface


## -description


Provides a mechanism for recipients of published events to restrict the number of event instances they receive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEventsFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesEventsFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesEventsFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">GetExcludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should not be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">GetIncludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b9d8339-3daa-4f0c-8a52-59e06b663163">GetPathFilter</a>
</td>
<td align="left" width="63%">
Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

