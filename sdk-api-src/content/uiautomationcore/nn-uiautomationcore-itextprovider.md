---
UID: NN:uiautomationcore.ITextProvider
title: ITextProvider
author: windows-sdk-content
description: Provides access to controls that contain text.
old-location: winauto\uiauto_ITextProvider.htm
old-project: WinAuto
ms.assetid: 8bd53f1e-731f-420b-a529-ca3f6c3fd97c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextProvider, ITextProvider interface [Windows Accessibility], ITextProvider interface [Windows Accessibility],described, uiauto.uiauto_ITextProvider, uiauto_ITextProvider, uiautomationcore/ITextProvider, winauto.uiauto_ITextProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
 - ITextProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextProvider interface


## -description


Provides access to controls that contain text.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITextProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5c0b2ed-e891-4856-8829-617a69d4708a">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc706d1d-b32d-4bc3-b65a-c42b38f06a93">GetVisibleRanges</a>
</td>
<td align="left" width="63%">
Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b55ae687-44e1-499f-8341-0bbf960529fd">RangeFromChild</a>
</td>
<td align="left" width="63%">
Retrieves a text range enclosing a child element such as an image, hyperlink, or other embedded object. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c19c6a4a-b783-47c2-8dfd-1ffe947278f0">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Returns the degenerate (empty) text range nearest to the specified screen coordinates. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/38892548-7c1f-4bac-8eac-29d7b4d190d3">DocumentRange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a text range that encloses the main text of a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1f91515-2bc8-4560-850d-34c880c78c43">SupportedTextSelection</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of text selection that is supported by the control.
        

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/4d541c31-11f7-4d7e-a0e0-9ed1da873d07">Text</a> control pattern.
		




## -see-also




<a href="https://msdn.microsoft.com/CDA6E93D-6E82-4EC4-8408-09554D039F49">ITextProvider2</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

