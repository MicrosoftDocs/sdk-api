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

# IAppxFactory2 interface


## -description


Creates objects for reading and writing app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFactory2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42453BD7-AB65-49E0-86C0-4F96B4234397">CreateContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/45C6F61E-8CF6-4188-9715-3954562F8AB0">IAppxContentGroupMapReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4BFF656D-4B89-4D05-9A41-44400F75E8BC">CreateContentGroupMapWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/A9B3992C-D3D1-4190-9314-A21E388E88BA">IAppxContentGroupMapWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB0FFB8D-A9DB-4B9C-B277-76623ECA3D6B">CreateSourceContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/EA0DF7E6-C4EF-4A58-A13F-EB3789239084">IAppxSourceContentGroupMapReader</a>.

</td>
</tr>
</table> 

