---
UID: NF:uiautomationclient.IUIAutomationElement3.get_CurrentIsPeripheral
title: IUIAutomationElement3::get_CurrentIsPeripheral
author: windows-sdk-content
description: Retrieves the current peripheral UI indicator for the element.
old-location: winauto\uiauto_IUIAutomationElement3_CurrentIsPeripheral.htm
old-project: WinAuto
ms.assetid: 1E4B7D77-FCE7-9A1B-2D1A-A347A2F8C2B9
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CurrentIsPeripheral property [Windows Accessibility], CurrentIsPeripheral property [Windows Accessibility],IUIAutomationElement3 interface, IUIAutomationElement3 interface [Windows Accessibility],CurrentIsPeripheral property, IUIAutomationElement3.CurrentIsPeripheral, IUIAutomationElement3.get_CurrentIsPeripheral, IUIAutomationElement3::CurrentIsPeripheral, IUIAutomationElement3::get_CurrentIsPeripheral, get_CurrentIsPeripheral, uiautomationclient/IUIAutomationElement3::CurrentIsPeripheral, uiautomationclient/IUIAutomationElement3::get_CurrentIsPeripheral, winauto.uiauto_IUIAutomationElement3_CurrentIsPeripheral
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement3.CurrentIsPeripheral
 - IUIAutomationElement3.get_CurrentIsPeripheral
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement3::get_CurrentIsPeripheral


## -description


Retrieves the current peripheral UI indicator for the element.

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
When client applications that are assistive technologies handle one of these events, the client should check the value of <b>CurrentIsPeripheral</b>. If the value is <b>TRUE</b>, the client may need to provide an alternative representation of the peripheral UI that the user can reach with a single action, because the client can't use changed focus as an indicator of new UI or a UI of interest. The peripheral UI won't otherwise exist in the control view, tab sequence and so on. A client is guaranteed that only one peripheral UI item exists in the overall tree at any one time, opening another would close the first one automatically.




## -see-also




<a href="https://msdn.microsoft.com/97AB327B-7A5D-C009-F430-42ADFC27F455">IUIAutomationElement3</a>



<b>Reference</b>
 

 

