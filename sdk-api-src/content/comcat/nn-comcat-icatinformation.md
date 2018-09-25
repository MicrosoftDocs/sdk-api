---
UID: NN:comcat.ICatInformation
title: ICatInformation
author: windows-sdk-content
description: Obtains information about the categories implemented or required by a certain class, as well as information about the categories registered on the specified computer.
old-location: com\icatinformation.htm
tech.root: com
ms.assetid: 1fd68126-b512-4131-8e93-cea7c1c3e9c0
ms.author: windowssdkdev
ms.date: 09/21/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICatInformation</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms693458(v=VS.85).aspx">EnumCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the component categories registered on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679677(v=VS.85).aspx">EnumClassesOfCategories</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the classes that implement one or more specified category identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687278(v=VS.85).aspx">EnumImplCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs implemented by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679728(v=VS.85).aspx">EnumReqCategoriesOfClass</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the CATIDs required by the specified class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684042(v=VS.85).aspx">GetCategoryDesc</a>
</td>
<td align="left" width="63%">
Retrieves the localized description string for a specific category ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686642(v=VS.85).aspx">IsClassOfCategories</a>
</td>
<td align="left" width="63%">
Determines whether a class implements one or more categories.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680737(v=VS.85).aspx">ICatRegister</a>
 

 

