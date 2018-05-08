---
UID: NN:uiautomationclient.IUIAutomationTextRange
title: IUIAutomationTextRange
author: windows-driver-content
description: Provides access to a span of continuous text in a container that supports the IUIAutomationTextPattern interface. Client applications can use the IUIAutomationTextRange interface to select, compare, and retrieve embedded objects from the text span.
old-location: winauto\uiauto_IUIAutomationTextRange.htm
old-project: WinAuto
ms.assetid: 1037919d-c8df-4d46-b3ce-62ee23c92145
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IUIAutomationTextRange, IUIAutomationTextRange interface [Windows Accessibility], IUIAutomationTextRange interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTextRange, uiauto_IUIAutomationTextRange, uiautomationclient/IUIAutomationTextRange, winauto.uiauto_IUIAutomationTextRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationTextRange
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange interface


## -description


Provides access to  a span of continuous text in a container that supports the <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a> interface. Client applications can use the <b>IUIAutomationTextRange</b> interface to select, compare, and retrieve embedded objects from the text span. The interface uses two endpoints to delimit where the text span starts and ends. Disjoint spans of text are represented by an <a href="https://msdn.microsoft.com/9f059173-7539-4164-b7af-182fa851d11a">IUIAutomationTextRangeArray</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTextRange</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5ae4a131-3283-4e91-8419-f2aa6f488833">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Retrieves a new <b>IUIAutomationTextRange</b> identical to the original and inheriting all properties of the original.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406436">Compare</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether this text range has the same endpoints as another text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7071ae46-3f2d-4fdb-9908-366ac1fde691">CompareEndpoints</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ec62c1-f738-43af-bd6c-b45fdfb32236">ExpandToEnclosingUnit</a>
</td>
<td align="left" width="63%">
Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12722d22-79ca-4390-8155-61234b821256">FindAttribute</a>
</td>
<td align="left" width="63%">
Retrieves a text range subset that has the specified text attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d6e9216-747b-45b5-90ac-ec19d36e5a0a">FindText</a>
</td>
<td align="left" width="63%">
Retrieves a text range subset that contains the specified text. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">GetAttributeValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified text attribute across the entire text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a155d143-c5ec-4669-9635-fb8f8012a684">GetBoundingRectangles</a>
</td>
<td align="left" width="63%">
Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/714e9d91-c6b9-4fa2-8a14-9bdd721b3135">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all embedded objects that fall within the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0120b4af-6f08-4bbd-b649-0f8e84cda3b9">GetEnclosingElement</a>
</td>
<td align="left" width="63%">
Returns the innermost UI Automation element that encloses the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Returns the plain text of the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b59ffdb5-6c05-4139-84ae-10ca5c543c3c">Move</a>
</td>
<td align="left" width="63%">
Moves the text range forward or backward by the specified number of text units .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16cb22ec-2735-41ab-88d5-78a27246af6e">MoveEndpointByRange</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the current text range to the specified endpoint of a second text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8724db1f-b8ed-4e00-9661-c22dd412653c">MoveEndpointByUnit</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the text range the specified number of text units within the document range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24aa2e4f-4024-4915-81f5-4bc704cc1559">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the text range from an existing collection of selected text in a text container that supports multiple, disjoint selections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d1ec553-1cc2-4b1c-a393-2507a3756a6c">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Causes the text control to scroll until the text range is visible in the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19e8dfe2-bf58-4ea1-8274-4e914f86ba07">Select</a>
</td>
<td align="left" width="63%">
Selects the span of text that corresponds to this text range, and removes any previous  selection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>



<a href="https://msdn.microsoft.com/66BC7324-5322-4996-AF62-766936559F0E">Using Text Ranges</a>
 

 

