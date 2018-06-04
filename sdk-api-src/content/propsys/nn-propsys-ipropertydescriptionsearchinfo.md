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

# IPropertyDescriptionSearchInfo interface


## -description



      Exposes search-related information for a property. The information provided by this interface comes from the <a href="shell.propdesc_schema_propertyDescription">propertyDescription</a> schema, <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element for a given property. This information is used by the Windows Search Indexer. Most calling applications will not need to call this interface.


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
<a href="shell.IPropertyDescriptionSearchInfo_GetColumnIndexType">GetColumnIndexType</a>
</td>
<td align="left" width="63%">
Determines the how the current property is indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionSearchInfo_GetMaxSize">GetMaxSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size value from the property schema's <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionSearchInfo_GetProjectionString">GetProjectionString</a>
</td>
<td align="left" width="63%">
Returns a pointer to a string containing the canonical name of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionSearchInfo_GetSearchInfoFlags">GetSearchInfoFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="shell.PROPDESC_SEARCHINFO_FLAGS">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.

</td>
</tr>
</table> 


## -see-also




<a href="shell.propdesc_schema_propertyDescription">propertyDescription</a>



<a href="shell.propdesc_schema_searchInfo">searchInfo</a>
 

 

