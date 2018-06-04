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

# ITpmVirtualSmartCardManager interface


## -description


Manages the TPM virtual smart cards.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITpmVirtualSmartCardManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITpmVirtualSmartCardManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITpmVirtualSmartCardManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C80C4DE2-0C43-40A5-81E6-7036A0B8DEB7">CreateVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Creates a TPM virtual smart card with the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8624CBF-FC39-4269-9405-8E7B5EE88F8D">DestroyVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Destroys the TPM virtual smart card that has the given instance ID.

</td>
</tr>
</table> 

