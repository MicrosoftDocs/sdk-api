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

# ICallFrameWalker interface


## -description


Walks a stack frame looking for interesting values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrameWalker</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICallFrameWalker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallFrameWalker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e599536f-87a3-4f71-ac0e-21bdafafd029">OnWalkInterface</a>
</td>
<td align="left" width="63%">
Walks through a call frame to look for the specified interface in the call frame.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/64e4967b-6b54-4416-ae10-04987f13d39a">ICallFrame::WalkFrame</a>
 

 

