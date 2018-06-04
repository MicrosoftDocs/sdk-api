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

# ITfFunction interface


## -description


The <b>ITfFunction</b> interface is the base interface for the individual function interfaces. This interface is implemented by the provider of the function object and used by any component to obtain the display name of the function object. Instances of this interface are not obtained directly. This interface is always part of a derived interface, such as <a href="https://msdn.microsoft.com/d5d60767-95f3-4ed0-b61e-58e06d1e1a98">ITfFnShowHelp</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFunction</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFunction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFunction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da52ca6d-9606-45c5-8db9-c876c827df14">GetDisplayName</a>
</td>
<td align="left" width="63%">
Obtains the function display name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d5d60767-95f3-4ed0-b61e-58e06d1e1a98">ITfFnShowHelp
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

