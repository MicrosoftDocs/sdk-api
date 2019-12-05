---
UID: NN:uiautomationclient.IUIAutomationNotificationEventHandler
title: IUIAutomationNotificationEventHandler (uiautomationclient.h)
description: Exposes a method to handle Microsoft UI Automation notification events.
old-location: winauto\uiauto_IUIAutomationNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: 7E12B8C2-D6A7-4637-9049-312B78EC01DE
ms.date: 12/05/2018
ms.keywords: IUIAutomationNotificationEventHandler, IUIAutomationNotificationEventHandler interface [Windows Accessibility], IUIAutomationNotificationEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationNotificationEventHandler, winauto.uiauto_IUIAutomationNotificationEventHandler
ms.topic: interface
f1_keywords:
- uiautomationclient/IUIAutomationNotificationEventHandler
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
- IUIAutomationNotificationEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationNotificationEventHandler interface


## -description


Exposes a method to handle Microsoft UI Automation notification events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationNotificationEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationNotificationEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationNotificationEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationnotificationeventhandler-handlenotificationevent">HandleNotificationEvent</a>
</td>
<td align="left" width="63%">
Handles a UI Automation notification event.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler">AddNotificationEventHandler</a>.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
 

 

