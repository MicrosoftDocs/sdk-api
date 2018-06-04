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

# IDelayedPropertyStoreFactory interface


## -description


Exposes a method to create a specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object in circumstances where property access is potentially slow.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDelayedPropertyStoreFactory</b> interface inherits from <a href="https://msdn.microsoft.com/78ea822d-da8e-4883-b0eb-4277e7eb87a2">IPropertyStoreFactory</a>. <b>IDelayedPropertyStoreFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDelayedPropertyStoreFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26df5fec-2a21-454e-9539-877c00a4f8fb">GetDelayedPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface object, as specified.

</td>
</tr>
</table> 

