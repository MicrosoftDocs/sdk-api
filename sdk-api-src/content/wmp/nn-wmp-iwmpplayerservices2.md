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

# IWMPPlayerServices2 interface


## -description



The <b>IWMPPlayerServices2</b> interface provides a method used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. In addition to the methods inherited from <b>IWMPPlayerServices</b>, the <b>IWMPPlayerServices2</b> interface exposes the following methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerServices2</b> interface inherits from <a href="https://msdn.microsoft.com/abbce425-9185-4235-8d8e-28be591be8e5">IWMPPlayerServices2</a>. <b>IWMPPlayerServices2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerServices2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e3536d2-006b-4019-a9c5-c460135cf555">setBackgroundProcessingPriority</a>
</td>
<td align="left" width="63%">
Specifies a priority level for general background processing tasks.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPPlayerServices2</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e">IWMPPlayerServices Interface</a>



<a href="https://msdn.microsoft.com/abbce425-9185-4235-8d8e-28be591be8e5">IWMPPlayerServices2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

