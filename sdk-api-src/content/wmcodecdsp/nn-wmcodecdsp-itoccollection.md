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

# ITocCollection interface


## -description


The <b>ITocCollection</b> represents a collection of tables of contents. It provides methods for adding, retrieving, and removing,  tables of contents from the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITocCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4d4e40b-151b-4217-81c8-1eaa8336407d">AddEntry</a>
</td>
<td align="left" width="63%">
Adds an individual table of contents  to the collection, and assigns an index to the added table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61f3103b-9b81-4729-a410-ab5ea63e072c">AddEntryByIndex</a>
</td>
<td align="left" width="63%">
Adds an individual table of contents to the collection, and associates a caller-supplied index with that table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93bddd4d-8a58-46e6-9284-eaa70be2c5a4">GetEntryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table of contents, specified by an index, from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/494efcde-cab3-4e72-9bc6-1df61f125f62">GetEntryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of tables of contents in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc6abad-2e9b-47f5-8b00-48ae480f3dd8">RemoveEntryByIndex</a>
</td>
<td align="left" width="63%">
 Removes a table of contents, specified by an index, from  the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/25039e6c-dd2a-4516-bf27-8e9d6ca0f00e">Table of Contents Parser Interfaces</a>
 

 

