---
UID: NN:uiautomationclient.IUIAutomationTextRange
title: IUIAutomationTextRange (uiautomationclient.h)

description: Provides access to a span of continuous text in a container that supports the IUIAutomationTextPattern interface. Client applications can use the IUIAutomationTextRange interface to select, compare, and retrieve embedded objects from the text span.
old-location: winauto\uiauto_IUIAutomationTextRange.htm
tech.root: WinAuto
ms.assetid: 1037919d-c8df-4d46-b3ce-62ee23c92145

ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange, IUIAutomationTextRange interface [Windows Accessibility], IUIAutomationTextRange interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTextRange, uiauto_IUIAutomationTextRange, uiautomationclient/IUIAutomationTextRange, winauto.uiauto_IUIAutomationTextRange
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationTextRange"
dev_langs:
 - c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTextRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextRange interface


## -description


Provides access to  a span of continuous text in a container that supports the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> interface. Client applications can use the <b>IUIAutomationTextRange</b> interface to select, compare, and retrieve embedded objects from the text span. The interface uses two endpoints to delimit where the text span starts and ends. Disjoint spans of text are represented by an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrangearray">IUIAutomationTextRangeArray</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRange</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTextRange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextRange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-addtoselection">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-clone">Clone</a>
</td>
<td align="left" width="63%">
Retrieves a new <b>IUIAutomationTextRange</b> identical to the original and inheriting all properties of the original.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-compare">Compare</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether this text range has the same endpoints as another text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints">CompareEndpoints</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit">ExpandToEnclosingUnit</a>
</td>
<td align="left" width="63%">
Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-findattribute">FindAttribute</a>
</td>
<td align="left" width="63%">
Retrieves a text range subset that has the specified text attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-findtext">FindText</a>
</td>
<td align="left" width="63%">
Retrieves a text range subset that contains the specified text. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue">GetAttributeValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified text attribute across the entire text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getboundingrectangles">GetBoundingRectangles</a>
</td>
<td align="left" width="63%">
Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all embedded objects that fall within the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement">GetEnclosingElement</a>
</td>
<td align="left" width="63%">
Returns the innermost UI Automation element that encloses the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-gettext">GetText</a>
</td>
<td align="left" width="63%">
Returns the plain text of the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-move">Move</a>
</td>
<td align="left" width="63%">
Moves the text range forward or backward by the specified number of text units .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange">MoveEndpointByRange</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the current text range to the specified endpoint of a second text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit">MoveEndpointByUnit</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the text range the specified number of text units within the document range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-removefromselection">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the text range from an existing collection of selected text in a text container that supports multiple, disjoint selections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Causes the text control to scroll until the text range is visible in the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-select">Select</a>
</td>
<td align="left" width="63%">
Selects the span of text that corresponds to this text range, and removes any previous  selection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-usingtextrangeobjects">Using Text Ranges</a>
 

 

