---
UID: NN:uiautomationclient.IUIAutomationNotificationEventHandler
title: IUIAutomationNotificationEventHandler (uiautomationclient.h)
description: Exposes a method to handle Microsoft UI Automation notification events.
helpviewer_keywords: ["IUIAutomationNotificationEventHandler","IUIAutomationNotificationEventHandler interface [Windows Accessibility]","IUIAutomationNotificationEventHandler interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationNotificationEventHandler","winauto.uiauto_IUIAutomationNotificationEventHandler"]
old-location: winauto\uiauto_IUIAutomationNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: 7E12B8C2-D6A7-4637-9049-312B78EC01DE
ms.date: 12/05/2018
ms.keywords: IUIAutomationNotificationEventHandler, IUIAutomationNotificationEventHandler interface [Windows Accessibility], IUIAutomationNotificationEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationNotificationEventHandler, winauto.uiauto_IUIAutomationNotificationEventHandler
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationNotificationEventHandler
 - uiautomationclient/IUIAutomationNotificationEventHandler
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
 - IUIAutomationNotificationEventHandler
---

# IUIAutomationNotificationEventHandler interface


## -description

Exposes a method to handle Microsoft UI Automation notification events.

## -inheritance

The <b>IUIAutomationNotificationEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationNotificationEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler">AddNotificationEventHandler</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
