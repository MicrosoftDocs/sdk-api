---
UID: NN:uiautomationcore.ITextRangeProvider
title: ITextRangeProvider
author: windows-sdk-content
description: Provides access to a span of continuous text in a text container that implements ITextProvider or ITextProvider2.
old-location: winauto\uiauto_ITextRangeProvider.htm
old-project: WinAuto
ms.assetid: dd14e608-1d21-4527-8b82-dba64ed04fda
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ITextRangeProvider, ITextRangeProvider interface [Windows Accessibility], ITextRangeProvider interface [Windows Accessibility],described, uiauto.uiauto_ITextRangeProvider, uiauto_ITextRangeProvider, uiautomationcore/ITextRangeProvider, winauto.uiauto_ITextRangeProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ITextRangeProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRangeProvider interface


## -description


Provides access to 
        a span of continuous text in a text container that implements <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a> or <a href="https://msdn.microsoft.com/CDA6E93D-6E82-4EC4-8408-09554D039F49">ITextProvider2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRangeProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextRangeProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e058ca62-6bb4-403e-a355-cc422a329109">AddToSelection</a>
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

        Returns a new <b>ITextRangeProvider</b> identical to the original 
        <b>ITextRangeProvider</b> and inheriting all properties of the original.
        

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
<a href="https://msdn.microsoft.com/88a59d93-f31b-40d5-a8d9-ef114224019b">CompareEndpoints</a>
</td>
<td align="left" width="63%">

        Returns a value that specifies whether two text ranges have identical endpoints.    
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6128b0ef-e78d-4f87-bc70-ab5ac0d055cf">ExpandToEnclosingUnit</a>
</td>
<td align="left" width="63%">

        Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/623a9b66-7d8c-44d7-b0c1-5ed8a8b8f0c6">FindAttribute</a>
</td>
<td align="left" width="63%">

        Returns a text range subset that has the specified text attribute value. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6012bc1e-5c1c-4874-ba2b-5e16eaf21f1d">FindText</a>
</td>
<td align="left" width="63%">

        Returns a text range subset that contains the specified text.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a72e780e-30e3-4feb-8f47-46b9f1714061">GetAttributeValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified text attribute across the text range.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ca1d170-538b-4dc2-83f3-850e1873c0d1">GetBoundingRectangles</a>
</td>
<td align="left" width="63%">

        Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b68a7eb-8ff5-4e8c-830b-e180b2c08be4">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all embedded objects that fall within the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51615c53-3239-41d6-895b-dbda68b6b4db">GetEnclosingElement</a>
</td>
<td align="left" width="63%">
Returns the innermost element that encloses the text range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Retrieves the plain text of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09cd8826-4fdf-4ea5-8159-18bb81e3b5cf">Move</a>
</td>
<td align="left" width="63%">
Moves the text range forward or backward by the specified number of text units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86411603-c37f-4192-95d1-8ac9b6ab6c44">MoveEndpointByRange</a>
</td>
<td align="left" width="63%">

        Moves one endpoint of the current text range to the specified endpoint of a second text range.  
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c0b9357-0f51-4044-8a5a-1f68af7a9762">MoveEndpointByUnit</a>
</td>
<td align="left" width="63%">
Moves one endpoint of the text range the specified number of <a href="https://msdn.microsoft.com/518318fc-d60f-41b7-a6da-1f2bf5c2e494">TextUnit</a> units within the document range.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057d784e-906a-4de8-bdd8-b58a2e26f37c">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the text range from the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58044de0-124f-4efd-a14f-4865f3278421">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Causes the text control to scroll vertically until the text range is visible in the viewport. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/486a604f-cea7-48de-aca2-2e9355699845">Select</a>
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



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

