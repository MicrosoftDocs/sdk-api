---
UID: NN:uiautomationclient.IUIAutomationNotificationEventHandler
title: IUIAutomationNotificationEventHandler
author: windows-sdk-content
description: Exposes a method to handle Microsoft UI Automation notification events.
old-location: winauto\uiauto_IUIAutomationNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: 7E12B8C2-D6A7-4637-9049-312B78EC01DE
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IUIAutomationNotificationEventHandler, IUIAutomationNotificationEventHandler interface [Windows Accessibility], IUIAutomationNotificationEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationNotificationEventHandler, winauto.uiauto_IUIAutomationNotificationEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationNotificationEventHandler interface


## -description


Exposes a method to handle Microsoft UI Automation notification events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationNotificationEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationNotificationEventHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A5FC58D4-B624-4EB1-9AC4-CD7C6F3BBFAE">HandleNotificationEvent</a>
</td>
<td align="left" width="63%">
Handles a UI Automation notification event.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by calling <a href="https://msdn.microsoft.com/1E6A4683-9439-4212-9EA6-91719A515C4B">AddNotificationEventHandler</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

