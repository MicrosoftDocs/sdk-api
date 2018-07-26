---
UID: NN:uiautomationcore.ILegacyIAccessibleProvider
title: ILegacyIAccessibleProvider
author: windows-sdk-content
description: Enables Microsoft UI Automation clients to access the underlying IAccessible implementation of Microsoft Active Accessibility elements.
old-location: winauto\uiauto_ILegacyIAccessibleProvider.htm
old-project: WinAuto
ms.assetid: 9d911238-05d9-4bba-920f-40ca23ab9549
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ILegacyIAccessibleProvider, ILegacyIAccessibleProvider interface [Windows Accessibility], ILegacyIAccessibleProvider interface [Windows Accessibility],described, uiauto.uiauto_ILegacyIAccessibleProvider, uiauto_ILegacyIAccessibleProvider, uiautomationcore/ILegacyIAccessibleProvider, winauto.uiauto_ILegacyIAccessibleProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ILegacyIAccessibleProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILegacyIAccessibleProvider interface


## -description


Enables Microsoft UI Automation clients to access the underlying <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> implementation of Microsoft Active Accessibility elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILegacyIAccessibleProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILegacyIAccessibleProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ILegacyIAccessibleProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29aaabba-dafe-400c-9fd6-80e13c0c9097">DoDefaultAction</a>
</td>
<td align="left" width="63%">
Performs the default action on the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d156866-d19a-4fd2-8664-d22e8b5434be">GetIAccessible</a>
</td>
<td align="left" width="63%">
Retrieves an accessible object that corresponds to a UI Automation element that supports the <a href="https://msdn.microsoft.com/4d66b9b8-ddbe-4bbc-b475-72dad1fe9393">LegacyIAccessible</a> control pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8436e554-2f09-46ed-a32a-0d2612bc60fb">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves the selected item or items in the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cdb3f88-c4aa-4a04-94e3-5549c389ad1f">Select</a>
</td>
<td align="left" width="63%">
Selects the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets the string value of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILegacyIAccessibleProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7dc1e5e8-050b-4a64-9a8e-cb0186878147">ChildId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the child identifier of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/10965fa1-1344-42d3-8466-d86bbad1f30d">DefaultAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains a description of the default action for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the description of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn926862">Help</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies a string  that contains help information for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cedb3a14-026f-4d2a-857f-313f4b5efad7">KeyboardShortcut</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the keyboard shortcut for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the name of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915787">Role</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the role identifier of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fe1a3ffe-b532-4bb4-850f-032fa32e4c56">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the state of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the value of this element.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the Microsoft Active Accessibility to UI Automation Proxy to expose native MSAA properties and methods to UI Automation clients that need them for legacy reasons. The proxy automatically supplies this interface for applications or controls that implement Microsoft Active Accessibility natively. This interface is not intended to be implemented by UI Automation applications or controls.
	



