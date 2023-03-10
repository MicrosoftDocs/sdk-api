---
UID: NN:uiautomationclient.IUIAutomationPropertyChangedEventHandler
title: IUIAutomationPropertyChangedEventHandler (uiautomationclient.h)
description: Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.
helpviewer_keywords: ["IUIAutomationPropertyChangedEventHandler","IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility]","IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationPropertyChangedEventHandler","uiauto_IUIAutomationPropertyChangedEventHandler","uiautomationclient/IUIAutomationPropertyChangedEventHandler","winauto.uiauto_IUIAutomationPropertyChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationPropertyChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: e89d1600-35f0-4baa-a32a-265a7ef82679
ms.date: 12/05/2018
ms.keywords: IUIAutomationPropertyChangedEventHandler, IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility], IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationPropertyChangedEventHandler, uiauto_IUIAutomationPropertyChangedEventHandler, uiautomationclient/IUIAutomationPropertyChangedEventHandler, winauto.uiauto_IUIAutomationPropertyChangedEventHandler
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
 - IUIAutomationPropertyChangedEventHandler
 - uiautomationclient/IUIAutomationPropertyChangedEventHandler
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
 - IUIAutomationPropertyChangedEventHandler
---

# IUIAutomationPropertyChangedEventHandler interface


## -description

Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.

## -inheritance

The <b>IUIAutomationPropertyChangedEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationPropertyChangedEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">AddPropertyChangedEventHandler</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
