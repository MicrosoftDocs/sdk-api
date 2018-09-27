---
UID: NN:propsys.IPropertyDescriptionSearchInfo
title: IPropertyDescriptionSearchInfo
author: windows-sdk-content
description: Exposes search-related information for a property.
old-location: properties\IPropertyDescriptionSearchInfo.htm
tech.root: properties
ms.assetid: 7bd4be80-7459-4c3d-9da4-0580995e6db6
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IPropertyDescriptionSearchInfo, IPropertyDescriptionSearchInfo interface [Windows Properties], IPropertyDescriptionSearchInfo interface [Windows Properties],described, _shell_IPropertyDescriptionSearchInfo, properties.IPropertyDescriptionSearchInfo, propsys/IPropertyDescriptionSearchInfo, shell.IPropertyDescriptionSearchInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IPropertyDescriptionSearchInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionSearchInfo interface


## -description


Exposes search-related information for a property. The information provided by this interface comes from the <a href="https://msdn.microsoft.com/en-us/library/Bb773880(v=VS.85).aspx">propertyDescription</a> schema, <a href="https://msdn.microsoft.com/en-us/library/Bb773885(v=VS.85).aspx">searchInfo</a> element for a given property. This information is used by the Windows Search Indexer. Most calling applications will not need to call this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionSearchInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyDescriptionSearchInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescriptionSearchInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761497(v=VS.85).aspx">GetColumnIndexType</a>
</td>
<td align="left" width="63%">
Determines the how the current property is indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761499(v=VS.85).aspx">GetMaxSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size value from the property schema's <a href="https://msdn.microsoft.com/en-us/library/Bb773885(v=VS.85).aspx">searchInfo</a> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761501(v=VS.85).aspx">GetProjectionString</a>
</td>
<td align="left" width="63%">
Returns a pointer to a string containing the canonical name of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761503(v=VS.85).aspx">GetSearchInfoFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb762588(v=VS.85).aspx">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773880(v=VS.85).aspx">propertyDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773885(v=VS.85).aspx">searchInfo</a>
 

 

