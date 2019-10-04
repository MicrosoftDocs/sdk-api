---
UID: NN:oleacc.IAccessible
title: IAccessible (oleacc.h)
author: windows-sdk-content
description: Exposes methods and properties that make a user interface element and its children accessible to client applications.
old-location: winauto\iaccessible.htm
tech.root: WinAuto
ms.assetid: 51e95b01-71e7-435b-85fb-28ee43eb08a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccessible, IAccessible interface [Windows Accessibility], IAccessible interface [Windows Accessibility],described, _msaa_IAccessible, msaa.iaccessible, oleacc/IAccessible, winauto.iaccessible
ms.topic: interface
f1_keywords: 
 - "oleacc/IAccessible"
dev_langs:
 - c++
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oleacc.h
api_name:
 - IAccessible
 - IAccessible.accName
 - IAccessible.get_accName
 - IAccessible.accValue
 - IAccessible.get_accValue
 - IAccessible.put_accValue
 - IAccessible.accChild
 - IAccessible.get_accChild
 - IAccessible.accChildCount
 - IAccessible.get_accChildCount
 - IAccessible.accDefaultAction
 - IAccessible.get_accDefaultAction
 - IAccessible.accDescription
 - IAccessible.get_accDescription
 - IAccessible.accFocus
 - IAccessible.get_accFocus
 - IAccessible.accHelp
 - IAccessible.get_accHelp
 - IAccessible.accHelpTopic
 - IAccessible.get_accHelpTopic
 - IAccessible.accKeyboardShortcut
 - IAccessible.get_accKeyboardShortcut
 - IAccessible.accParent
 - IAccessible.get_accParent
 - IAccessible.accRole
 - IAccessible.get_accRole
 - IAccessible.accSelection
 - IAccessible.get_accSelection
 - IAccessible.accState
 - IAccessible.get_accState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessible interface


## -description


Exposes methods and properties that make a user interface element and its children accessible to client applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessible</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAccessible</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAccessible</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accdodefaultaction">accDoDefaultAction</a>
</td>
<td align="left" width="63%">
Performs the specified object's default action. Not all objects have a default action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acchittest">accHitTest</a>
</td>
<td align="left" width="63%">
Retrieves the child element or child object at a given point on the screen. All visual objects support this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acclocation">accLocation</a>
</td>
<td align="left" width="63%">
Retrieves the specified object's current screen location. All visual objects support this method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accnavigate">accNavigate</a>
</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accnavigate">accNavigate</a>method is deprecated and should not be used. Clients should use other methods and properties such as <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-accessiblechildren">AccessibleChildren</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">get_accParent</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/implementing-the-ienumvariant-interface">IEnumVARIANT</a>.</div>
<div> </div>
Traverses to another user interface element within a container and retrieves the object. All visual objects support this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accselect">accSelect</a>
</td>
<td align="left" width="63%">
Modifies the selection or moves the keyboard focus of the specified object. 
	 All objects that support selection or receive the keyboard focus must support this method.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessible</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accChild</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An <a href="https://docs.microsoft.com/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface for the specified child, if one exists. 
	 All objects must support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accChildCount</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of children that belong to this object. All objects must support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchildcount">get_accChildCount</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accDefaultAction</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A string that describes the object's default action. Not all objects have a default action. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accdefaultaction">get_accDefaultAction</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accDescription</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accdescription">accDescription</a> property is not supported in the transition to UI Automation. Microsoft Active Accessibility servers and applications should not use it. </div>
<div> </div>
A string that describes the visual appearance of the specified object. Not all objects have a description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accFocus</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The object that has the keyboard focus. All objects that receive the keyboard focus must support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accfocus">get_accFocus</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accHelp</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A help string. Not all objects support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acchelp">get_accHelp</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accHelpTopic</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
<div class="alert"><b>Note</b>  The <b>accHelpTopic</b> property is deprecated and should not be used.</div>
<div> </div>
 The full path of the help file associated with the specified object and the identifier of the appropriate topic within that file. 
	 Not all objects support this property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accKeyboardShortcut</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The object's shortcut key or access key, also known as the mnemonic. All objects that have a shortcut key or an access key support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut">get_accKeyboardShortcut</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accName</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the object. All objects support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accname">get_accName</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accParent</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface of the object's parent. All objects support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">get_accParent</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accRole</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Information that describes the role of the specified object. All objects support this property.
See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accrole">get_accRole</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accSelection</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The selected children of this object. All objects that support selection must support this property.
See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accselection">get_accSelection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accState</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The current state of the object. All objects support this property. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accstate">get_accState</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>accValue</b>

</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The value of the object. Not all objects have a value. See <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accvalue">get_accValue</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-put_accvalue">put_accValue</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>
 

 

