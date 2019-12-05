---
UID: NN:comcat.ICatInformation
title: ICatInformation (comcat.h)
description: Obtains information about the categories implemented or required by a certain class, as well as information about the categories registered on the specified computer.
old-location: com\icatinformation.htm
tech.root: com
ms.assetid: 1fd68126-b512-4131-8e93-cea7c1c3e9c0
ms.date: 12/05/2018
ms.keywords: ICatInformation, ICatInformation interface [COM], ICatInformation interface [COM],described, _com_icatinformation, com.icatinformation, comcat/ICatInformation
ms.topic: interface
f1_keywords:
- comcat/ICatInformation
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICatInformation interface


## -description


Obtains information about the categories implemented or required by a certain class, as well as information about the categories registered on the specified computer.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICatInformation</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-enumcategories">EnumCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the component categories registered on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-enumclassesofcategories">EnumClassesOfCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the classes that implement one or more specified category identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-enumimplcategoriesofclass">EnumImplCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs implemented by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-enumreqcategoriesofclass">EnumReqCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs required by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-getcategorydesc">GetCategoryDesc</a>
</td>
<td align="left" width="63%">
Retrieves the localized description string for a specific category ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatinformation-isclassofcategories">IsClassOfCategories</a>
</td>
<td align="left" width="63%">
Determines whether a class implements one or more categories.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>
 

 

