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

# ISBE2GlobalEvent2 interface


## -description


Offers  access to global spanning events and their data from the <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filters.  A <i>global spanning event</i> contains state information that applies to all the streams in a pipeline. This interface extends the <a href="https://msdn.microsoft.com/18bb9f8a-df97-468c-acb2-be7fa61a4789">ISBE2GlobalEvent</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2GlobalEvent2</b> interface inherits from <b>ISBE2GlobalEvent</b>. <b>ISBE2GlobalEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2GlobalEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44c30d8a-d62b-4e0f-8ff9-a4159df6d724">GetEventEx</a>
</td>
<td align="left" width="63%">
Gets an global spanning event and its data from a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.



</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2GlobalEvent2)</code>.



