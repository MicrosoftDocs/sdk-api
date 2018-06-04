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

# ICatInformation interface


## -description


Obtains information about the categories implemented or required by a certain class, as well as information about the categories registered on the specified computer.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatInformation</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICatInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICatInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8e744f0-6e50-4260-89df-e2cc59937398">EnumCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the component categories registered on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13d470ff-77e6-4a17-b2c9-c53676e21fba">EnumClassesOfCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the classes that implement one or more specified category identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82d938b0-c05d-4bd9-b33f-c7944ed1399b">EnumImplCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs implemented by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bde9359-6d0e-4d8f-9c9b-ceabaf2da61f">EnumReqCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs required by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f004c2-2616-441e-8bb7-f56eb062bb35">GetCategoryDesc</a>
</td>
<td align="left" width="63%">
Retrieves the localized description string for a specific category ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/772d4d75-2076-4922-bf47-2e6e41a5687d">IsClassOfCategories</a>
</td>
<td align="left" width="63%">
Determines whether a class implements one or more categories.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

