---
UID: NN:uiautomationcore.ISelectionItemProvider
title: ISelectionItemProvider (uiautomationcore.h)
description: Provides access to individual, selectable child controls of containers that implement ISelectionProvider.
old-location: winauto\uiauto_ISelectionItemProvider.htm
tech.root: WinAuto
ms.assetid: 464b05e3-06da-44b9-b4a6-c64452fcdb6d
ms.date: 12/05/2018
ms.keywords: ISelectionItemProvider, ISelectionItemProvider interface [Windows Accessibility], ISelectionItemProvider interface [Windows Accessibility],described, uiauto.uiauto_ISelectionItemProvider, uiauto_ISelectionItemProvider, uiautomationcore/ISelectionItemProvider, winauto.uiauto_ISelectionItemProvider
f1_keywords:
- uiautomationcore/ISelectionItemProvider
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
- ISelectionItemProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISelectionItemProvider interface


## -description


Provides 
        access to individual, selectable child controls of containers that implement 
        <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionprovider">ISelectionProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionItemProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISelectionItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISelectionItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionitemprovider-addtoselection">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the current element to the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionitemprovider-removefromselection">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the current element from the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionitemprovider-select">Select</a>
</td>
<td align="left" width="63%">
Deselects any selected items and then selects the current element. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionItemProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionitemprovider-get_isselected">IsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether an item is selected. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer">SelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the provider that implements <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionprovider">ISelectionProvider</a> 
        and acts as the container for the calling object.
        

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that 
            must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingselectionitem">SelectionItem</a> control pattern.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

