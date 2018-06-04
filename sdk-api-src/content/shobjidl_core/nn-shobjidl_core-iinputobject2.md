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

# IInputObject2 interface


## -description


Exposes a method that extends <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a> by handling global accelerators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputObject2</b> interface inherits from <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a>. <b>IInputObject2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputObject2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f55f2671-7164-421e-9269-aa70e85180de">TranslateAcceleratorGlobal</a>
</td>
<td align="left" width="63%">
Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a> interface, from which it inherits.



