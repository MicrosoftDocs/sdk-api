---
UID: NN:d2d1svg.ID2D1SvgElement
title: ID2D1SvgElement
author: windows-sdk-content
description: Interface for all SVG elements.
old-location: direct2d\id2d1svgelement.htm
tech.root: Direct2D
ms.assetid: 19099DC9-EA14-41C5-A9DF-5EBB12696C79
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1SvgElement, ID2D1SvgElement interface [Direct2D], ID2D1SvgElement interface [Direct2D],described, d2d1svg/ID2D1SvgElement, direct2d.id2d1svgelement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement interface


## -description


Interface for all SVG elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgElement</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1SvgElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BE9F0820-D66E-4B20-8790-3D5B3652754B">AppendChild</a>
</td>
<td align="left" width="63%">
Appends an element to the list of children. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E8BD0808-D3A3-41BB-A7A3-2183C0E56396">CreateChild</a>
</td>
<td align="left" width="63%">
Creates an element from a tag name. The element is appended to the list of children. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f6ca40a-6c78-9c60-c06a-a31f6edf7663">GetAttributeValue</a>
</td>
<td align="left" width="63%">Overloaded. Gets an attribute of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B466C04-7768-4F15-AC68-55A3074499C1">GetAttributeValueLength</a>
</td>
<td align="left" width="63%">
Gets the string length of an attribute of this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87ACD0CD-AF31-4734-80F7-67090154D5D1">GetDocument</a>
</td>
<td align="left" width="63%">
Gets the document that contains this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EA233AE-CC2C-442D-A8CE-FF3DC645785A">GetFirstChild</a>
</td>
<td align="left" width="63%">
Gets the first child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA100037-7177-4547-B161-D52E059A5F35">GetLastChild</a>
</td>
<td align="left" width="63%">
Gets the last child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41D48F64-3C90-4CB1-91F5-32FC04042471">GetNextChild</a>
</td>
<td align="left" width="63%">
Gets the next sibling of the referenceChild element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1396BEE3-23F1-4C07-8A74-BF07F14AB093">GetParent</a>
</td>
<td align="left" width="63%">
Gets the parent element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CE4334D8-7A96-464A-BE57-A7B226221FC3">GetPreviousChild</a>
</td>
<td align="left" width="63%">
Gets the previous sibling of the referenceChild element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB683CA6-57B5-4B13-9EB3-269DDCA94667">GetSpecifiedAttributeCount</a>
</td>
<td align="left" width="63%">
Returns the number of specified attributes on this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08419C4C-4EED-406F-884C-84532C6AF1CC">GetSpecifiedAttributeName</a>
</td>
<td align="left" width="63%">
Gets the name of the attribute at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AD94B020-D9AA-4B1F-B7C3-DEF97DADFEEA">GetSpecifiedAttributeNameLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the name of the specified attribute at the given index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00E1D15D-6976-40F2-880C-0F0D90B767D6">GetTagName</a>
</td>
<td align="left" width="63%">
Gets the tag name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD73B8E6-4490-4BF2-9A65-6661DB3594E1">GetTagNameLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the tag name. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97B396BE-467A-4B5D-A87B-8B2B8BC6E71D">GetTextValue</a>
</td>
<td align="left" width="63%">
Gets the value of a text content element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC644B2A-3DBF-46D7-B5A3-88FD0BC51D38">GetTextValueLength</a>
</td>
<td align="left" width="63%">
Gets the length of the text content value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E7942E1-AD67-44B5-9C8D-89DD7551BA18">HasChildren</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating whether this element has children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09BBABC1-0644-473E-A751-C84437941A2B">InsertChildBefore</a>
</td>
<td align="left" width="63%">
Inserts newChild as a child of this element, before the referenceChild element.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94B91C4E-B2E5-4E23-B381-5920EA0F8F31">IsAttributeSpecified</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating if the attribute is explicitly set on the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AB2078AC-033F-4111-B67D-014EF439E2B5">IsTextContent</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating wether this element represents text content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/608BB970-CC78-4CF3-BD8C-02DCBBFA287E">RemoveAttribute</a>
</td>
<td align="left" width="63%">
Removes the attribute from this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/986EE898-D377-4DFF-B19E-834D5CD1A4E6">RemoveChild</a>
</td>
<td align="left" width="63%">
Removes the oldChild from the tree. Children of oldChild remain children of oldChild.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BEF74F58-D218-46CA-AE02-F15DDAC48FB4">ReplaceChild</a>
</td>
<td align="left" width="63%">
Replaces the oldChild element with the newChild.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33403a07-28d1-4138-ea7f-04f3ac42a8f7">SetAttributeValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets an attribute of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/569257CB-1B85-458D-92F4-EBE6C3FF0639">SetTextValue</a>
</td>
<td align="left" width="63%">
Sets the value of a text content element.

</td>
</tr>
</table> 

