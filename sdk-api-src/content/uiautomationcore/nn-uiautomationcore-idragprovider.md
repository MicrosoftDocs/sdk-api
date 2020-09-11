---
UID: NN:uiautomationcore.IDragProvider
title: IDragProvider (uiautomationcore.h)
description: Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.
helpviewer_keywords: ["IDragProvider","IDragProvider interface [Windows Accessibility]","IDragProvider interface [Windows Accessibility]","described","uiautomationcore/IDragProvider","winauto.uiauto_idragprovider"]
old-location: winauto\uiauto_idragprovider.htm
tech.root: WinAuto
ms.assetid: FAC4A56D-17BC-42E6-A03E-EE45D717DE37
ms.date: 12/05/2018
ms.keywords: IDragProvider, IDragProvider interface [Windows Accessibility], IDragProvider interface [Windows Accessibility],described, uiautomationcore/IDragProvider, winauto.uiauto_idragprovider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IDragProvider
 - uiautomationcore/IDragProvider
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
 - IDragProvider
---

# IDragProvider interface


## -description

Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDragProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDragProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-getgrabbeditems">GetGrabbedItems</a>
</td>
<td align="left" width="63%">
Retrieves the collection of elements that are being dragged as part of a drag operation.  

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffect">DropEffect</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffects">DropEffects</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element is dropped as part of a drag-and-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_isgrabbed">IsGrabbed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element has been grabbed as part of a drag-and-drop operation.

</td>
</tr>
</table>

## -remarks

A provider can implement <b>IDragProvider</b> only on the element being dragged, or it can use an intermediary drag object that implements <b>IDragProvider</b>, in addition to the <b>IDragProvider</b> implementation on the individual element.  The intermediary is responsible for firing all events, which enables the provider to support dragging multiple elements at once, and to describe the multi-element drag operation with a single set of drag properties and events.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider">IDropTargetProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/ui-automation-support-for-drag-and-drop">UI Automation Support for Drag-and-Drop</a>

