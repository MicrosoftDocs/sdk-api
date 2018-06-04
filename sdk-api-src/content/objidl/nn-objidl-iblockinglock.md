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

# IBlockingLock interface


## -description


Provides a semaphore that can be used to provide temporarily exclusive access to a shared resource such as a file.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBlockingLock</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IBlockingLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBlockingLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35657795-2f18-4738-b0b5-8d03e0e4179d">Lock</a>
</td>
<td align="left" width="63%">
Requests a lock on a shared resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/152c2d72-fa49-4213-8916-81a6383900cc">Unlock</a>
</td>
<td align="left" width="63%">
Releases a lock on a shared resource.

</td>
</tr>
</table> 

