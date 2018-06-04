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

# IOleCacheControl interface


## -description


Provides proper maintenance of caches. It maintains the caches by connecting the running object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> implementation to the cache, allowing the cache to receive notifications from the running object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleCacheControl</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleCacheControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleCacheControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d155c3f-115c-41fe-985f-ed60a565341f">OnRun</a>
</td>
<td align="left" width="63%">
Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b">OnStop</a>
</td>
<td align="left" width="63%">
Notifies the cache that it should terminate any existing advise sinks.

</td>
</tr>
</table> 

