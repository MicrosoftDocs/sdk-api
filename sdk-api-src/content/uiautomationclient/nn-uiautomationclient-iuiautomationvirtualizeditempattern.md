---
UID: NN:uiautomationclient.IUIAutomationVirtualizedItemPattern
title: IUIAutomationVirtualizedItemPattern (uiautomationclient.h)
description: Represents a virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.
helpviewer_keywords: ["IUIAutomationVirtualizedItemPattern","IUIAutomationVirtualizedItemPattern interface [Windows Accessibility]","IUIAutomationVirtualizedItemPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationVirtualizedItemPattern","uiauto_IUIAutomationVirtualizedItemPattern","uiautomationclient/IUIAutomationVirtualizedItemPattern","winauto.uiauto_IUIAutomationVirtualizedItemPattern"]
old-location: winauto\uiauto_IUIAutomationVirtualizedItemPattern.htm
tech.root: WinAuto
ms.assetid: 48f066f3-c78c-47a2-9668-ab79b1438130
ms.date: 12/05/2018
ms.keywords: IUIAutomationVirtualizedItemPattern, IUIAutomationVirtualizedItemPattern interface [Windows Accessibility], IUIAutomationVirtualizedItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationVirtualizedItemPattern, uiauto_IUIAutomationVirtualizedItemPattern, uiautomationclient/IUIAutomationVirtualizedItemPattern, winauto.uiauto_IUIAutomationVirtualizedItemPattern
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationVirtualizedItemPattern
 - uiautomationclient/IUIAutomationVirtualizedItemPattern
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
 - IUIAutomationVirtualizedItemPattern
---

# IUIAutomationVirtualizedItemPattern interface


## -description

Represents a virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.

## -inheritance

The <b>IUIAutomationVirtualizedItemPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationVirtualizedItemPattern</b> also has these types of members:

## -remarks

A virtualized item can be an item retrieved from a control that supports the <a href="/windows/desktop/WinAuto/uiauto-implementingitemcontainer">ItemContainer</a> control pattern, or a virtualized embedded object retrieved from a control that supports the <a href="/windows/desktop/WinAuto/uiauto-about-text-and-textrange-patterns">Text</a> control pattern.

The placeholder automation element for a virtualized item might not have loaded data for all UI Automation properties, and may return <a href="/windows/desktop/WinAuto/uiauto-error-codes">UIA_E_ELEMENTNOTAVAILABLE</a> in response to queries for properties that are not available.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="/windows/desktop/WinAuto/uiauto-workingwithvirtualizeditems">Working with Virtualized Items</a>
