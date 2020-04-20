---
UID: NN:uiautomationcore.IRawElementProviderFragment
title: IRawElementProviderFragment (uiautomationcore.h)
description: Exposes methods and properties on UI elements that are part of a structure more than one level deep, such as a list box or list item. Implemented by Microsoft UI Automation provider.helpviewer_keywords: ["IRawElementProviderFragment","IRawElementProviderFragment interface [Windows Accessibility]","IRawElementProviderFragment interface [Windows Accessibility]","described","uiauto.uiauto_IRawElementProviderFragment","uiauto_IRawElementProviderFragment","uiautomationcore/IRawElementProviderFragment","winauto.uiauto_IRawElementProviderFragment"]
old-location: winauto\uiauto_IRawElementProviderFragment.htm
tech.root: WinAuto
ms.assetid: 63539ba9-7f13-48cf-9c8a-74c03d31e2ab
ms.date: 12/05/2018
ms.keywords: IRawElementProviderFragment, IRawElementProviderFragment interface [Windows Accessibility], IRawElementProviderFragment interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderFragment, uiauto_IRawElementProviderFragment, uiautomationcore/IRawElementProviderFragment, winauto.uiauto_IRawElementProviderFragment
f1_keywords:
- uiautomationcore/IRawElementProviderFragment
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IRawElementProviderFragment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRawElementProviderFragment interface


## -description


Exposes methods and properties on UI elements that are part of a structure more than one level deep, 
		such as a list box or list item. Implemented by Microsoft UI Automation provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragment</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderFragment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRawElementProviderFragment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots">GetEmbeddedFragmentRoots</a>
</td>
<td align="left" width="63%">
Retrieves an array of root fragments that are embedded in the UI Automation tree rooted at the current element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the runtime identifier of an element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-navigate">Navigate</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element in a specified direction within the UI Automation tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the focus to this element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragment</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle">BoundingRectangle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the bounding rectangle of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-get_fragmentroot">FragmentRoot</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the root node of the fragment.

</td>
</tr>
</table> 


## -remarks



The root node of the fragment must also support the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>



<b>Reference</b>
 

 

