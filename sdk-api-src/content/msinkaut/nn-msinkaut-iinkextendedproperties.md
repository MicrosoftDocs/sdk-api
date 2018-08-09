---
UID: NN:msinkaut.IInkExtendedProperties
title: IInkExtendedProperties
author: windows-sdk-content
description: Represents a collection of IInkExtendedProperty objects that contain application-defined data.
old-location: tablet\iinkextendedproperties.htm
old-project: tablet
ms.assetid: c7b7f40f-0c28-4848-83d6-d5db73eef998
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInkExtendedProperties, IInkExtendedProperties interface [Tablet PC], IInkExtendedProperties interface [Tablet PC],described, c7b7f40f-0c28-4848-83d6-d5db73eef998, msinkaut/IInkExtendedProperties, tablet.iinkextendedproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkExtendedProperties interface


## -description



Represents a collection of <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> objects that contain application-defined data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkExtendedProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkExtendedProperties</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Specifies the extended property to add to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears all of the extended properties from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/285d6ce3-f7f9-48b0-aaa2-d9ff8db732eb">DoesPropertyExist</a>
</td>
<td align="left" width="63%">
Specifies whether an extended property exists within a collection of extended properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Specifies the extended property to return at the known index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
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
Gets either the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b> property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> objects in the collection.

</td>
</tr>
</table> 


## -remarks



The extended property data is indexed by an application-specific globally unique identifier (GUID).

<div class="alert"><b>Note</b>  You cannot store an empty <b>IInkExtendedProperties</b> object. The object must contain data before it can be stored. For example, if you try to add extended properties to a stroke for later use, an exception is thrown if the extended property contains no data.</div>
<div> </div>
<b>IInkExtendedProperties</b> collections may be added to the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a>, the <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a>, and the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> objects.

For more information about collections in Automation, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/6263770e-741d-4b4f-b33f-f808b7816622">ExtendedProperties Property</a>



<a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty Interface</a>
 

 

