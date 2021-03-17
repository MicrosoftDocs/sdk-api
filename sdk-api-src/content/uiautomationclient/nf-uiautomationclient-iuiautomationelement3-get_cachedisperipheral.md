---
UID: NF:uiautomationclient.IUIAutomationElement3.get_CachedIsPeripheral
title: IUIAutomationElement3::get_CachedIsPeripheral (uiautomationclient.h)
description: Retrieves the cached peripheral UI indicator for the element.
helpviewer_keywords: ["CachedIsPeripheral property [Windows Accessibility]","CachedIsPeripheral property [Windows Accessibility]","IUIAutomationElement3 interface","IUIAutomationElement3 interface [Windows Accessibility]","CachedIsPeripheral property","IUIAutomationElement3.CachedIsPeripheral","IUIAutomationElement3.get_CachedIsPeripheral","IUIAutomationElement3::CachedIsPeripheral","IUIAutomationElement3::get_CachedIsPeripheral","get_CachedIsPeripheral","uiautomationclient/IUIAutomationElement3::CachedIsPeripheral","uiautomationclient/IUIAutomationElement3::get_CachedIsPeripheral","winauto.uiauto_IUIAutomationElement3_CachedIsPeripheral"]
old-location: winauto\uiauto_IUIAutomationElement3_CachedIsPeripheral.htm
tech.root: WinAuto
ms.assetid: 3F6D2EE1-CE3B-2E48-7539-555A44D1DBFD
ms.date: 12/05/2018
ms.keywords: CachedIsPeripheral property [Windows Accessibility], CachedIsPeripheral property [Windows Accessibility],IUIAutomationElement3 interface, IUIAutomationElement3 interface [Windows Accessibility],CachedIsPeripheral property, IUIAutomationElement3.CachedIsPeripheral, IUIAutomationElement3.get_CachedIsPeripheral, IUIAutomationElement3::CachedIsPeripheral, IUIAutomationElement3::get_CachedIsPeripheral, get_CachedIsPeripheral, uiautomationclient/IUIAutomationElement3::CachedIsPeripheral, uiautomationclient/IUIAutomationElement3::get_CachedIsPeripheral, winauto.uiauto_IUIAutomationElement3_CachedIsPeripheral
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement3::get_CachedIsPeripheral
 - uiautomationclient/IUIAutomationElement3::get_CachedIsPeripheral
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement3.CachedIsPeripheral
 - IUIAutomationElement3.get_CachedIsPeripheral
---

# IUIAutomationElement3::get_CachedIsPeripheral


## -description

Retrieves the cached peripheral UI indicator for the element. Peripheral UI appears and supports user interaction, but does not take keyboard focus when it appears.  Examples of peripheral UI includes popups, flyouts, context menus, or floating notifications. 

This property is read-only.

## -parameters

## -remarks

When the <b>IsPeripheral</b> property is <b>TRUE</b>, a client application can't assume that focus was taken by the element even if it's currently keyboard-interactive.

This property is relevant for these control types:

<ul>
<li><b>UIA_GroupControlTypeId</b></li>
<li><b>UIA_MenuControlTypeId</b></li>
<li><b>UIA_PaneControlTypeId</b></li>
<li><b>UIA_ToolBarControlTypeId</b></li>
<li><b>UIA_ToolTipControlTypeId</b></li>
<li><b>UIA_WindowControlTypeId</b></li>
<li><b>UIA_CustomControlTypeId</b></li>
</ul>
The appearance of peripheral UI often triggers one of these events, if the peripheral UI supports one of the relevant patterns:

<ul>
<li><b>WindowOpened</b> (<b>UIA_Window_WindowOpenedEventId</b>)</li>
<li><b>MenuOpened</b> (<b>UIA_MenuOpenedEventId</b>)</li>
<li><b>ToolTipOpened</b> (<b>UIA_ToolTipOpenedEventId</b>)</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement3">IUIAutomationElement3</a>



<b>Reference</b>