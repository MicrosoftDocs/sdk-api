---
UID: NN:msinkaut.IInkExtendedProperties
title: IInkExtendedProperties (msinkaut.h)
description: Represents a collection of IInkExtendedProperty objects that contain application-defined data.helpviewer_keywords: ["IInkExtendedProperties","IInkExtendedProperties interface [Tablet PC]","IInkExtendedProperties interface [Tablet PC]","described","c7b7f40f-0c28-4848-83d6-d5db73eef998","msinkaut/IInkExtendedProperties","tablet.iinkextendedproperties"]
old-location: tablet\iinkextendedproperties.htm
tech.root: tablet
ms.assetid: c7b7f40f-0c28-4848-83d6-d5db73eef998
ms.date: 12/05/2018
ms.keywords: IInkExtendedProperties, IInkExtendedProperties interface [Tablet PC], IInkExtendedProperties interface [Tablet PC],described, c7b7f40f-0c28-4848-83d6-d5db73eef998, msinkaut/IInkExtendedProperties, tablet.iinkextendedproperties
f1_keywords:
- msinkaut/IInkExtendedProperties
dev_langs:
- c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkExtendedProperties
- IInkExtendedProperties._NewEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkExtendedProperties interface


## -description



Represents a collection of <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> objects that contain application-defined data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkExtendedProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkExtendedProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkExtendedProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-add">Add</a>
</td>
<td align="left" width="63%">
Specifies the extended property to add to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears all of the extended properties from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-doespropertyexist">DoesPropertyExist</a>
</td>
<td align="left" width="63%">
Specifies whether an extended property exists within a collection of extended properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-item">Item</a>
</td>
<td align="left" width="63%">
Specifies the extended property to return at the known index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-remove">Remove</a>
</td>
<td align="left" width="63%">
Specifies the extended property to remove from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkExtendedProperties</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>_NewEnum</b>

</td>
<td align="left" width="10%">


</td>
<td align="left" width="63%">
Gets either the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b> property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> objects in the collection.

</td>
</tr>
</table> 


## -remarks



The extended property data is indexed by an application-specific globally unique identifier (GUID).

<div class="alert"><b>Note</b>  You cannot store an empty <b>IInkExtendedProperties</b> object. The object must contain data before it can be stored. For example, if you try to add extended properties to a stroke for later use, an exception is thrown if the extended property contains no data.</div>
<div> </div>
<b>IInkExtendedProperties</b> collections may be added to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a>, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a>, and the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> objects.

For more information about collections in Automation, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties">ExtendedProperties Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty Interface</a>
 

 

