---
UID: NN:uiautomationclient.IUIAutomationVirtualizedItemPattern
title: IUIAutomationVirtualizedItemPattern (uiautomationclient.h)
description: Represents an virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.
old-location: winauto\uiauto_IUIAutomationVirtualizedItemPattern.htm
tech.root: WinAuto
ms.assetid: 48f066f3-c78c-47a2-9668-ab79b1438130
ms.date: 12/05/2018
ms.keywords: IUIAutomationVirtualizedItemPattern, IUIAutomationVirtualizedItemPattern interface [Windows Accessibility], IUIAutomationVirtualizedItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationVirtualizedItemPattern, uiauto_IUIAutomationVirtualizedItemPattern, uiautomationclient/IUIAutomationVirtualizedItemPattern, winauto.uiauto_IUIAutomationVirtualizedItemPattern
f1_keywords:
- uiautomationclient/IUIAutomationVirtualizedItemPattern
dev_langs:
- c++
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
- IUIAutomationVirtualizedItemPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationVirtualizedItemPattern interface


## -description


Represents an virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationVirtualizedItemPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationVirtualizedItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationVirtualizedItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize">Realize</a>
</td>
<td align="left" width="63%">
Creates a full UI Automation element for a virtualized item.

</td>
</tr>
</table> 


## -remarks



A virtualized item can be an item retrieved from a control that supports the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingitemcontainer">ItemContainer</a> control pattern, or a virtualized embedded object retrieved from a control that supports the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-about-text-and-textrange-patterns">Text</a> control pattern.

The placeholder automation element for a virtualized item might not have loaded data for all UI Automation properties, and may return <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-error-codes">UIA_E_ELEMENTNOTAVAILABLE</a> in response to queries for properties that are not available.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithvirtualizeditems">Working with Virtualized Items</a>
 

 

