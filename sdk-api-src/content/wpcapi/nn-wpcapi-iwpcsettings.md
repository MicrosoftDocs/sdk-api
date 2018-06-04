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

# IWPCSettings interface


## -description


Accesses general settings for the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWPCSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fe5be0c-e6fa-481d-a28d-c5b15257b901">GetLastSettingsChangeTime</a>
</td>
<td align="left" width="63%">
Retrieves the time at which the configuration settings were last updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22350ef3-3068-4d33-a023-74644e5fbb83">GetRestrictions</a>
</td>
<td align="left" width="63%">
Determines whether web restrictions, time limits, or game restrictions are on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfe04843-af23-4146-bc45-f91d6ad36c1a">IsLoggingRequired</a>
</td>
<td align="left" width="63%">
Determines whether activity logging should be performed when obtaining the <b>IWPCSettings</b> interface.

</td>
</tr>
</table> 

