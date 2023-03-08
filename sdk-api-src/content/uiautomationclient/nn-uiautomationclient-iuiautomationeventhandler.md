---
UID: NN:uiautomationclient.IUIAutomationEventHandler
title: IUIAutomationEventHandler (uiautomationclient.h)
description: Exposes a method to handle Microsoft UI Automation events.
helpviewer_keywords: ["IUIAutomationEventHandler","IUIAutomationEventHandler interface [Windows Accessibility]","IUIAutomationEventHandler interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationEventHandler","uiauto_IUIAutomationEventHandler","uiautomationclient/IUIAutomationEventHandler","winauto.uiauto_IUIAutomationEventHandler"]
old-location: winauto\uiauto_IUIAutomationEventHandler.htm
tech.root: WinAuto
ms.assetid: 3b79e085-fb38-403d-b7f1-3e7680f3449f
ms.date: 12/05/2018
ms.keywords: IUIAutomationEventHandler, IUIAutomationEventHandler interface [Windows Accessibility], IUIAutomationEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationEventHandler, uiauto_IUIAutomationEventHandler, uiautomationclient/IUIAutomationEventHandler, winauto.uiauto_IUIAutomationEventHandler
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
 - IUIAutomationEventHandler
 - uiautomationclient/IUIAutomationEventHandler
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
 - IUIAutomationEventHandler
---

# IUIAutomationEventHandler interface


## -description

Exposes a method to handle Microsoft UI Automation events.

## -inheritance

The <b>IUIAutomationEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addautomationeventhandler">AddAutomationEventHandler</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
