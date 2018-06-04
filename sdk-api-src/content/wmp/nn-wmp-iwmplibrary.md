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

# IWMPLibrary interface


## -description



The <b>IWMPLibrary</b> interface represents a library.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de39a4e-fcce-401b-9bbf-7b06d1fb0370">get_mediaCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMPMediacollection</b> interface for the current library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28f1e3bc-3692-4fd0-a0b3-fecc3a173103">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the current library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95f36972-2227-4fe8-88d7-41f7aebbf67a">get_type</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the library type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af121fc7-6a9a-4c1a-bea4-433e62ca19e3">isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the supplied object is the same as the current one.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/766cfd4e-53e6-44a8-87e6-2b9c1fa2ff3f">IWMPLibraryServices::getLibraryByType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

