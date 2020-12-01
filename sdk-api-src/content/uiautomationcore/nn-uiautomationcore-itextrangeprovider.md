---
UID: NN:uiautomationcore.ITextRangeProvider
title: ITextRangeProvider (uiautomationcore.h)
description: Provides access to a span of continuous text in a text container that implements ITextProvider or ITextProvider2.
helpviewer_keywords: ["ITextRangeProvider","ITextRangeProvider interface [Windows Accessibility]","ITextRangeProvider interface [Windows Accessibility]","described","uiauto.uiauto_ITextRangeProvider","uiauto_ITextRangeProvider","uiautomationcore/ITextRangeProvider","winauto.uiauto_ITextRangeProvider"]
old-location: winauto\uiauto_ITextRangeProvider.htm
tech.root: WinAuto
ms.assetid: dd14e608-1d21-4527-8b82-dba64ed04fda
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider, ITextRangeProvider interface [Windows Accessibility], ITextRangeProvider interface [Windows Accessibility],described, uiauto.uiauto_ITextRangeProvider, uiauto_ITextRangeProvider, uiautomationcore/ITextRangeProvider, winauto.uiauto_ITextRangeProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRangeProvider
 - uiautomationcore/ITextRangeProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ITextRangeProvider
---

# ITextRangeProvider interface


## -description

Provides access to 
        a span of continuous text in a text container that implements <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a> or <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2">ITextProvider2</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRangeProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextRangeProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextRangeProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-addtoselection">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-clone">Clone</a>
</td>
<td align="left" width="63%">
Returns a new <b>ITextRangeProvider</b> identical to the original 
        <b>ITextRangeProvider</b> and inheriting all properties of the original.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare">Compare</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether this text range has the same endpoints as another text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints">CompareEndpoints</a>
</td>
<td align="left" width="63%">
Returns a value that specifies whether two text ranges have identical endpoints.    
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit">ExpandToEnclosingUnit</a>
</td>
<td align="left" width="63%">
Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-findattribute">FindAttribute</a>
</td>
<td align="left" width="63%">
Returns a text range subset that has the specified text attribute value. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-findtext">FindText</a>
</td>
<td align="left" width="63%">
Returns a text range subset that contains the specified text.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getattributevalue">GetAttributeValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified text attribute across the text range.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles">GetBoundingRectangles</a>
</td>
<td align="left" width="63%">
Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all embedded objects that fall within the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getenclosingelement">GetEnclosingElement</a>
</td>
<td align="left" width="63%">
Returns the innermost element that encloses the text range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-gettext">GetText</a>
</td>
<td align="left" width="63%">
Retrieves the plain text of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-move">Move</a>
</td>
<td align="left" width="63%">
Moves the text range forward or backward by the specified number of text units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange">MoveEndpointByRange</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the current text range to the specified endpoint of a second text range.  
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit">MoveEndpointByUnit</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the text range the specified number of <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a> units within the document range.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-removefromselection">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the text range from the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-scrollintoview">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Causes the text control to scroll vertically until the text range is visible in the viewport. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-select">Select</a>
</td>
<td align="left" width="63%">
Selects the span of text that corresponds to this text range, and removes any previous  selection. 

</td>
</tr>
</table>

## -remarks

A range can represent an insertion point, a portion of text, or all of the text in a container.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>