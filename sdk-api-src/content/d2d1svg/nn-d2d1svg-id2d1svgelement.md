---
UID: NN:d2d1svg.ID2D1SvgElement
title: ID2D1SvgElement (d2d1svg.h)
author: windows-sdk-content
description: Interface for all SVG elements.
old-location: direct2d\id2d1svgelement.htm
tech.root: Direct2D
ms.assetid: 19099DC9-EA14-41C5-A9DF-5EBB12696C79
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement, ID2D1SvgElement interface [Direct2D], ID2D1SvgElement interface [Direct2D],described, d2d1svg/ID2D1SvgElement, direct2d.id2d1svgelement
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
ms.custom: 19H1
---

# ID2D1SvgElement interface


## -description


Interface for all SVG elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgElement</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1SvgElement</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-appendchild">AppendChild</a>
</td>
<td align="left" width="63%">
Appends an element to the list of children. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-createchild">CreateChild</a>
</td>
<td align="left" width="63%">
Creates an element from a tag name. The element is appended to the list of children. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1svgelement-getattributevalue-overload">GetAttributeValue</a>
</td>
<td align="left" width="63%">Overloaded. Gets an attribute of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevaluelength">GetAttributeValueLength</a>
</td>
<td align="left" width="63%">
Gets the string length of an attribute of this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getdocument">GetDocument</a>
</td>
<td align="left" width="63%">
Gets the document that contains this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getfirstchild">GetFirstChild</a>
</td>
<td align="left" width="63%">
Gets the first child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getlastchild">GetLastChild</a>
</td>
<td align="left" width="63%">
Gets the last child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getnextchild">GetNextChild</a>
</td>
<td align="left" width="63%">
Gets the next sibling of the referenceChild element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getparent">GetParent</a>
</td>
<td align="left" width="63%">
Gets the parent element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getpreviouschild">GetPreviousChild</a>
</td>
<td align="left" width="63%">
Gets the previous sibling of the referenceChild element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getspecifiedattributecount">GetSpecifiedAttributeCount</a>
</td>
<td align="left" width="63%">
Returns the number of specified attributes on this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getspecifiedattributename">GetSpecifiedAttributeName</a>
</td>
<td align="left" width="63%">
Gets the name of the attribute at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getspecifiedattributenamelength">GetSpecifiedAttributeNameLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the name of the specified attribute at the given index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-gettagname">GetTagName</a>
</td>
<td align="left" width="63%">
Gets the tag name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-gettagnamelength">GetTagNameLength</a>
</td>
<td align="left" width="63%">
Gets the string length of the tag name. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-gettextvalue">GetTextValue</a>
</td>
<td align="left" width="63%">
Gets the value of a text content element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-gettextvaluelength">GetTextValueLength</a>
</td>
<td align="left" width="63%">
Gets the length of the text content value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-haschildren">HasChildren</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating whether this element has children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-insertchildbefore">InsertChildBefore</a>
</td>
<td align="left" width="63%">
Inserts newChild as a child of this element, before the referenceChild element.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-isattributespecified">IsAttributeSpecified</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating if the attribute is explicitly set on the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-istextcontent">IsTextContent</a>
</td>
<td align="left" width="63%">
Returns a boolean indicating wether this element represents text content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-removeattribute">RemoveAttribute</a>
</td>
<td align="left" width="63%">
Removes the attribute from this element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-removechild">RemoveChild</a>
</td>
<td align="left" width="63%">
Removes the oldChild from the tree. Children of oldChild remain children of oldChild.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-replacechild">ReplaceChild</a>
</td>
<td align="left" width="63%">
Replaces the oldChild element with the newChild.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-setattributevalue">SetAttributeValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets an attribute of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-settextvalue">SetTextValue</a>
</td>
<td align="left" width="63%">
Sets the value of a text content element.

</td>
</tr>
</table> 

