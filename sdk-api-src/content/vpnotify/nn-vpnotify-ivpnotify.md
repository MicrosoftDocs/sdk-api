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

# IVPNotify interface


## -description



Supports a private communication mechanism between the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter and a VPE decoder filter that represents a hardware decoder.

Only the Overlay Mixer filter implements this interface. Applications should never use it.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPNotify</b> interface inherits from <a href="https://msdn.microsoft.com/c72bd662-366c-4102-9ad9-9e4c59096ede">IVPBaseNotify</a>. <b>IVPNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08d28857-5460-407d-a169-8568b2c381e6">GetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing mode (such as bob or weave).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41984fb1-7276-4232-b19a-d251c9fcd699">SetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Sets the deinterlacing mode (such as bob or weave).

</td>
</tr>
</table> 


## -remarks




        Include Vptype.h before Vpnotify.h.
      




## -see-also




<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a>



<a href="https://msdn.microsoft.com/c72bd662-366c-4102-9ad9-9e4c59096ede">IVPBaseNotify</a>



<a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig</a>
 

 

