---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

