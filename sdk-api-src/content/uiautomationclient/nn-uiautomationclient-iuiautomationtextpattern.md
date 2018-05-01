---
UID: NN:uiautomationclient.IUIAutomationTextPattern
title: IUIAutomationTextPattern
author: windows-driver-content
description: Provides access to a control that contains text.
old-location: winauto\uiauto_IUIAutomationTextPattern.htm
old-project: WinAuto
ms.assetid: ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IUIAutomationTextPattern, IUIAutomationTextPattern interface [Windows Accessibility], IUIAutomationTextPattern interface [Windows Accessibility], described, uiauto.uiauto_IUIAutomationTextPattern, uiauto_IUIAutomationTextPattern, uiautomationclient/IUIAutomationTextPattern, winauto.uiauto_IUIAutomationTextPattern
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
-	IUIAutomationTextPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextPattern interface


## -description


Provides access to a control that contains text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTextPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTextPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2aca7414-afb2-402d-80cf-d7ce3e719b20">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cf4e6d4-223c-4222-a181-c16a5a90ef65">GetVisibleRanges</a>
</td>
<td align="left" width="63%">
Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e75d21da-129f-4209-b51b-777ca5880946">RangeFromChild</a>
</td>
<td align="left" width="63%">
Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa80b1d8-c50e-45be-8769-8b937c8e714a">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4234260a-6b3d-4f63-9082-9e225c614410">DocumentRange</a>


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

<a href="https://msdn.microsoft.com/794c08d4-9305-4fdd-8ca0-188e1e9b6547">SupportedTextSelection</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of text selection that is supported by the control.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

