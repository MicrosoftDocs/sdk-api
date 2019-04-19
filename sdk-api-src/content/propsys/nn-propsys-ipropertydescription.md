---
UID: NN:propsys.IPropertyDescription
title: IPropertyDescription (propsys.h)
author: windows-sdk-content
description: Exposes methods that enumerate and retrieve individual property description details.
old-location: properties\IPropertyDescription.htm
tech.root: properties
ms.assetid: 9abd476c-450e-4381-b28e-afca00d4b179
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyDescription, IPropertyDescription interface [Windows Properties], IPropertyDescription interface [Windows Properties],described, properties.IPropertyDescription, propsys/IPropertyDescription, shell.IPropertyDescription, shell_IPropertyDescription
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
 - IPropertyDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyDescription interface


## -description


Exposes methods that enumerate and retrieve individual property description details.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescription</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyDescription</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescription</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761519(v=VS.85).aspx">CoerceToCanonicalValue</a>
</td>
<td align="left" width="63%">
Coerces the value to the canonical value, according to the property description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761521(v=VS.85).aspx">FormatForDisplay</a>
</td>
<td align="left" width="63%">
Gets a formatted, Unicode string representation of a property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761523(v=VS.85).aspx">GetAggregationType</a>
</td>
<td align="left" width="63%">
Gets a value that describes how the property values are displayed when multiple items are selected in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761525(v=VS.85).aspx">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Gets the case-sensitive name by which a property is known to the system, regardless of its localized name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761527(v=VS.85).aspx">GetColumnState</a>
</td>
<td align="left" width="63%">
Gets the column state flag, which describes how the property should be treated by interfaces or APIs that use this flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761529(v=VS.85).aspx">GetConditionType</a>
</td>
<td align="left" width="63%">
Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761531(v=VS.85).aspx">GetDefaultColumnWidth</a>
</td>
<td align="left" width="63%">
Gets the default column width of the property in a list view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms712505(v=VS.85).aspx">GetDisplayName</a>
</td>
<td align="left" width="63%">
Gets the display name of the property as it is shown in any UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761535(v=VS.85).aspx">GetDisplayType</a>
</td>
<td align="left" width="63%">
Gets the current data type used to display the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761538(v=VS.85).aspx">GetEditInvitation</a>
</td>
<td align="left" width="63%">
Gets the text used in edit controls hosted in various dialog boxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761539(v=VS.85).aspx">GetEnumTypeList</a>
</td>
<td align="left" width="63%">
Gets an instance of an <a href="https://msdn.microsoft.com/en-us/library/Bb761483(v=VS.85).aspx">IPropertyEnumTypeList</a>, which can be used to enumerate the possible values for a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761542(v=VS.85).aspx">GetGroupingRange</a>
</td>
<td align="left" width="63%">
Gets the grouping method to be used when a view is grouped by a property, and retrieves the grouping type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761544(v=VS.85).aspx">GetPropertyKey</a>
</td>
<td align="left" width="63%">
Gets a structure that acts as a property's unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff800945(v=VS.85).aspx">GetPropertyType</a>
</td>
<td align="left" width="63%">
Gets the variant type of the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761547(v=VS.85).aspx">GetRelativeDescription</a>
</td>
<td align="left" width="63%">
Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761549(v=VS.85).aspx">GetRelativeDescriptionType</a>
</td>
<td align="left" width="63%">
Gets the relative description type for a property description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761551(v=VS.85).aspx">GetSortDescription</a>
</td>
<td align="left" width="63%">
Gets the current sort description flags for the property, which indicate the particular wordings of sort offerings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761553(v=VS.85).aspx">GetSortDescriptionLabel</a>
</td>
<td align="left" width="63%">
Gets the localized display string that describes the current sort order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761556(v=VS.85).aspx">GetTypeFlags</a>
</td>
<td align="left" width="63%">
Gets a set of flags that describe the uses and capabilities of the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761559(v=VS.85).aspx">GetViewFlags</a>
</td>
<td align="left" width="63%">
Gets the current set of flags governing the property's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761563(v=VS.85).aspx">IsValueCanonical</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether a property is canonical according to the definition of the property description.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> in the system; it is provided by the Shell. 

To obtain this interface, call <a href="https://msdn.microsoft.com/en-us/library/Bb776503(v=VS.85).aspx">PSGetPropertyDescription</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb776504(v=VS.85).aspx">PSGetPropertyDescriptionByName</a>, or <a href="https://msdn.microsoft.com/library/Bb761507(v=VS.85).aspx">IPropertyDescriptionList::GetAt</a>.

Only one property description exists for each property in the system.




## -see-also




<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

