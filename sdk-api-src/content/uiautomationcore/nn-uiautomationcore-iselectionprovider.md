---
UID: NN:uiautomationcore.ISelectionProvider
title: ISelectionProvider (uiautomationcore.h)
description: Provides access to controls that act as containers for a collection of individual, selectable child items.
old-location: winauto\uiauto_ISelectionProvider.htm
tech.root: WinAuto
ms.assetid: e02731f8-e58d-4c66-95bf-005cf954471c
ms.date: 12/05/2018
ms.keywords: ISelectionProvider, ISelectionProvider interface [Windows Accessibility], ISelectionProvider interface [Windows Accessibility],described, uiauto.uiauto_ISelectionProvider, uiauto_ISelectionProvider, uiautomationcore/ISelectionProvider, winauto.uiauto_ISelectionProvider
ms.topic: interface
f1_keywords:
- uiautomationcore/ISelectionProvider
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
- ISelectionProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISelectionProvider interface


## -description


Provides access 
        to controls that act as containers for a collection of individual, selectable child items. 
        The children of this control must implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISelectionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISelectionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionprovider-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation provider for each child element that is selected.
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple">CanSelectMultiple</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the UI Automation provider 
        allows more than one child element to be selected concurrently.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired">IsSelectionRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the UI Automation provider requires at least one child element to be selected.
        

</td>
</tr>
</table> 


## -remarks



This interface is implemented by a UI Automation provider.

Providers should raise an event of type <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">UIA_Selection_InvalidatedEventId</a> when a selection in a container has changed significantly.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

