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

# IPersistStreamInit interface


## -description


A replacement for <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> that adds an initialization method.

This interface is not derived from <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>; it is mutually exclusive with <b>IPersistStream</b>. An object chooses to support only one of the two interfaces, based on whether it requires the <a href="https://msdn.microsoft.com/9e318698-0c3c-41c2-bb9e-04e8c9746c4d">InitNew</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistStreamInit</b> interface inherits from <b>IPersist</b>. <b>IPersistStreamInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistStreamInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8413eeda-3867-4352-aefb-82579a4861f2">GetSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves the size of the stream needed to save the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e318698-0c3c-41c2-bb9e-04e8c9746c4d">InitNew</a>
</td>
<td align="left" width="63%">
Initializes an object to a default state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b84818d-0d9d-4f55-8031-b4336baa6c09">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e995e07-e088-40de-ba28-c30caea45786">Load</a>
</td>
<td align="left" width="63%">
Initializes an object from the stream where it was saved previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Saves an object to the specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
 

 

