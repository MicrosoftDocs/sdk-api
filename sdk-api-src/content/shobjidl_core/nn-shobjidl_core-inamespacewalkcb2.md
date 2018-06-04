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

# INamespaceWalkCB2 interface


## -description


Extends <a href="https://msdn.microsoft.com/15244d6e-6cd7-4dee-8e4e-2533d5a60ae7">INamespaceWalkCB</a> with a method that is required in order to complete a namespace walk. This method removes data collected during the walk.    


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamespaceWalkCB2</b> interface inherits from <a href="https://msdn.microsoft.com/15244d6e-6cd7-4dee-8e4e-2533d5a60ae7">INamespaceWalkCB</a>. <b>INamespaceWalkCB2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamespaceWalkCB2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a41d460-71c9-4add-86e4-8ce27b3632d0">WalkComplete</a>
</td>
<td align="left" width="63%">
Removes data collected during a namespace walk.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/15244d6e-6cd7-4dee-8e4e-2533d5a60ae7">INamespaceWalkCB</a> interface, from which it inherits.




## -see-also




<a href="https://msdn.microsoft.com/164732ae-1c72-465c-a16b-a8eeaa9cc185">INamespaceWalk</a>



<a href="https://msdn.microsoft.com/15244d6e-6cd7-4dee-8e4e-2533d5a60ae7">INamespaceWalkCB</a>
 

 

