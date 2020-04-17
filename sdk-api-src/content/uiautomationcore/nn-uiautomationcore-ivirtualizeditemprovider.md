---
UID: NN:uiautomationcore.IVirtualizedItemProvider
title: IVirtualizedItemProvider (uiautomationcore.h)
description: Provides access to virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.helpviewer_keywords: ["IVirtualizedItemProvider","IVirtualizedItemProvider interface [Windows Accessibility]","IVirtualizedItemProvider interface [Windows Accessibility]","described","uiauto.uiauto_IVirtualizedItemProvider","uiauto_IVirtualizedItemProvider","uiautomationcore/IVirtualizedItemProvider","winauto.uiauto_IVirtualizedItemProvider"]
old-location: winauto\uiauto_IVirtualizedItemProvider.htm
tech.root: WinAuto
ms.assetid: 39baaa54-b836-497c-b401-a865202626e7
ms.date: 12/05/2018
ms.keywords: IVirtualizedItemProvider, IVirtualizedItemProvider interface [Windows Accessibility], IVirtualizedItemProvider interface [Windows Accessibility],described, uiauto.uiauto_IVirtualizedItemProvider, uiauto_IVirtualizedItemProvider, uiautomationcore/IVirtualizedItemProvider, winauto.uiauto_IVirtualizedItemProvider
f1_keywords:
- uiautomationcore/IVirtualizedItemProvider
dev_langs:
- c++
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
- IVirtualizedItemProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVirtualizedItemProvider interface


## -description


Provides access to virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualizedItemProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVirtualizedItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVirtualizedItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivirtualizeditemprovider-realize">Realize</a>
</td>
<td align="left" width="63%">
Makes the virtual item fully accessible as a UI Automation element.

</td>
</tr>
</table> 


## -remarks



A virtualized item is typically an item in a virtual list; that is, a list that does not manage its own data. When an application retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> for a virtualized item by using <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty">FindItemByProperty</a>, UI Automation calls the provider's implementation of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty">FindItemByProperty</a>, where the provider may return a placeholder element that also implements <b>IVirtualizedItemProvider</b>. On a call to <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize">Realize</a>, the provider's implementation of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivirtualizeditemprovider-realize">Realize</a> returns a full UI Automation element reference and may also scroll the item into view.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingvirtualizeditem">VirtualizedItem Control Pattern</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithvirtualizeditems">Working with Virtualized Items</a>
 

 

