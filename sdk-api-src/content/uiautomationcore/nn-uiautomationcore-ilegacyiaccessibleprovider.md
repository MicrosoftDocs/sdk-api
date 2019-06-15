---
UID: NN:uiautomationcore.ILegacyIAccessibleProvider
title: ILegacyIAccessibleProvider (uiautomationcore.h)
author: windows-sdk-content
description: Enables Microsoft UI Automation clients to access the underlying IAccessible implementation of Microsoft Active Accessibility elements.
old-location: winauto\uiauto_ILegacyIAccessibleProvider.htm
tech.root: WinAuto
ms.assetid: 9d911238-05d9-4bba-920f-40ca23ab9549
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILegacyIAccessibleProvider, ILegacyIAccessibleProvider interface [Windows Accessibility], ILegacyIAccessibleProvider interface [Windows Accessibility],described, uiauto.uiauto_ILegacyIAccessibleProvider, uiauto_ILegacyIAccessibleProvider, uiautomationcore/ILegacyIAccessibleProvider, winauto.uiauto_ILegacyIAccessibleProvider
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
 - ILegacyIAccessibleProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILegacyIAccessibleProvider interface


## -description


Enables Microsoft UI Automation clients to access the underlying <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> implementation of Microsoft Active Accessibility elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILegacyIAccessibleProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILegacyIAccessibleProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction">DoDefaultAction</a>
</td>
<td align="left" width="63%">
Performs the default action on the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible">GetIAccessible</a>
</td>
<td align="left" width="63%">
Retrieves an accessible object that corresponds to a UI Automation element that supports the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementinglegacyiaccessible">LegacyIAccessible</a> control pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves the selected item or items in the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-select">Select</a>
</td>
<td align="left" width="63%">
Selects the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue">SetValue</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid">ChildId</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction">DefaultAction</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description">Description</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help">Help</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut">KeyboardShortcut</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role">Role</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state">State</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value">Value</a>


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
	



