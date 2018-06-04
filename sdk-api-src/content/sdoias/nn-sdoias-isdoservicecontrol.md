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

# ISdoServiceControl interface


## -description


Use the 
<b>ISdoServiceControl</b> interface to control the service being administered on the SDO computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoServiceControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISdoServiceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdoServiceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ef65e85-d77d-4f59-aaac-c0b5b337b564">GetServiceStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93675ad-b7c2-42b9-9ab8-7fb4cbb7a07c">ResetService</a>
</td>
<td align="left" width="63%">
Resets the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f024a3b8-c527-4a43-99df-c5b146dae1b8">StartService</a>
</td>
<td align="left" width="63%">
Starts the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a90e4d12-589b-4d28-89e6-6c0ec6900b0a">StopService</a>
</td>
<td align="left" width="63%">
Stops the service.

</td>
</tr>
</table> 


## -remarks



Use the 
<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a> method to retrieve a pointer to an 
<b>ISdoServiceControl</b> interface.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa">Server Data Objects Interfaces</a>



<a href="https://msdn.microsoft.com/0a73adfb-3f4b-46f6-8b76-d48f8599e05d">Server Data Objects Reference</a>
 

 

