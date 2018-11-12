---
UID: NN:comcat.ICatInformation
title: ICatInformation
author: windows-sdk-content
description: Obtains information about the categories implemented or required by a certain class, as well as information about the categories registered on the specified computer.
old-location: com\icatinformation.htm
tech.root: com
ms.assetid: 1fd68126-b512-4131-8e93-cea7c1c3e9c0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICatInformation, ICatInformation interface [COM], ICatInformation interface [COM],described, _com_icatinformation, com.icatinformation, comcat/ICatInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - ICatInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

