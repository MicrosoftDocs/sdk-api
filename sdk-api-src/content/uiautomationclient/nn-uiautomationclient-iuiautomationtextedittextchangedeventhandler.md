---
UID: NN:uiautomationclient.IUIAutomationTextEditTextChangedEventHandler
title: IUIAutomationTextEditTextChangedEventHandler (uiautomationclient.h)
description: Exposes a method to handle events that occur when Microsoft UI Automation reports a text-changed event from text edit controls.
helpviewer_keywords: ["IUIAutomationTextEditTextChangedEventHandler","IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility]","IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationTextEditTextChangedEventHandler","winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationTextEditTextChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 1308F513-5458-900C-A494-9AC9131C2D1E
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextEditTextChangedEventHandler, IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility], IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTextEditTextChangedEventHandler
 - uiautomationclient/IUIAutomationTextEditTextChangedEventHandler
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
 - IUIAutomationTextEditTextChangedEventHandler
 - IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
---

# IUIAutomationTextEditTextChangedEventHandler interface


## -description

Exposes a method to handle events that occur when Microsoft UI Automation reports a text-changed event from text edit controls.

## -inheritance

The <b>IUIAutomationTextEditTextChangedEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTextEditTextChangedEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by using <b>AddTextEditTextChangedEventHandler</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
