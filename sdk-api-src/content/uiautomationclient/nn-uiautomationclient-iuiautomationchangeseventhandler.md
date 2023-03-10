---
UID: NN:uiautomationclient.IUIAutomationChangesEventHandler
title: IUIAutomationChangesEventHandler (uiautomationclient.h)
description: Exposes a method to handle one or more Microsoft UI Automation change events.
helpviewer_keywords: ["IUIAutomationChangesEventHandler","IUIAutomationChangesEventHandler interface [Windows Accessibility]","IUIAutomationChangesEventHandler interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationChangesEventHandler","winauto.uiauto_IUIAutomationChangesEventHandler"]
old-location: winauto\uiauto_IUIAutomationChangesEventHandler.htm
tech.root: WinAuto
ms.assetid: 8DCF8826-B688-416C-9195-34E0290054AA
ms.date: 12/05/2018
ms.keywords: IUIAutomationChangesEventHandler, IUIAutomationChangesEventHandler interface [Windows Accessibility], IUIAutomationChangesEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationChangesEventHandler, winauto.uiauto_IUIAutomationChangesEventHandler
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
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationChangesEventHandler
 - uiautomationclient/IUIAutomationChangesEventHandler
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
 - IUIAutomationChangesEventHandler
---

# IUIAutomationChangesEventHandler interface


## -description

Exposes a method to handle one or more Microsoft UI Automation change events.

## -inheritance

The <b>IUIAutomationChangesEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationChangesEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-addchangeseventhandler">AddChangesEventHandler</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
