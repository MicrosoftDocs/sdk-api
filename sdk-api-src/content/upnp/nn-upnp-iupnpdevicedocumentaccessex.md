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

# IUPnPDeviceDocumentAccessEx interface


## -description


The <b>IUPnPDeviceDocumentAccessEx</b> interface provides a method to obtain the entire XML device description document for a specific device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceDocumentAccessEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceDocumentAccessEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceDocumentAccessEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12778bd4-9e62-42a4-b9b3-29ee9c6d2d40">GetDocument</a>
</td>
<td align="left" width="63%">
Retrieves the XML device description document for a UPnP device.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling QueryInterface on the same object that provides an implementation of <a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>, after which <a href="https://msdn.microsoft.com/12778bd4-9e62-42a4-b9b3-29ee9c6d2d40">GetDocument</a> can be called on it.




## -see-also




<a href="https://msdn.microsoft.com/6f73bf8c-0423-430f-a654-58d076712aae">Control Point API Reference</a>



<a href="https://msdn.microsoft.com/6d71425e-3e33-44e0-845a-4bcd05939d24">IUPnPDeviceDocumentAccess</a>
 

 

