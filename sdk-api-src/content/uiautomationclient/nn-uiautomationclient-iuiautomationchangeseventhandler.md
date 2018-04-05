---
UID: NN:uiautomationclient.IUIAutomationChangesEventHandler
title: IUIAutomationChangesEventHandler
author: windows-driver-content
description: Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.
old-location: winauto\uiauto_IUIAutomationChangesEventHandler.htm
old-project: WinAuto
ms.assetid: 8DCF8826-B688-416C-9195-34E0290054AA
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IUIAutomationChangesEventHandler, IUIAutomationChangesEventHandler interface [Windows Accessibility], IUIAutomationChangesEventHandler interface [Windows Accessibility], described, uiautomationclient/IUIAutomationChangesEventHandler, winauto.uiauto_IUIAutomationChangesEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationChangesEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationChangesEventHandler interface


## -description


Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationChangesEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationChangesEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationChangesEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5BCE09F7-9811-49F5-B2C4-8DABC44CA406">HandleChangesEvent</a>
</td>
<td align="left" width="63%">
Handles a UI Automation changes event.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by calling <a href="https://msdn.microsoft.com/E479ACCA-9372-463F-A992-8030E33A2341">AddChangesEventHandler</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

