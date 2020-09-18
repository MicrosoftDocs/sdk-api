---
UID: NN:uiautomationclient.IUIAutomationActiveTextPositionChangedEventHandler
title: IUIAutomationActiveTextPositionChangedEventHandler (uiautomationclient.h)
description: Exposes a method to handle Microsoft UI Automation events that occur when the active text position changes.
helpviewer_keywords: ["IUIAutomationActiveTextPositionChangedEventHandler","IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility]","IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler","winauto.uiauto_IUIAutomationActiveTextPositionChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 038AD911-2FDB-42E5-86E0-76C58F765114
ms.date: 12/05/2018
ms.keywords: IUIAutomationActiveTextPositionChangedEventHandler, IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility], IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomationActiveTextPositionChangedEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - IUIAutomationActiveTextPositionChangedEventHandler
 - uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler
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
 - IUIAutomationActiveTextPositionChangedEventHandler
---

# IUIAutomationActiveTextPositionChangedEventHandler interface


## -description

Exposes a method to handle Microsoft UI Automation events that occur when the active text position changes.<div class="alert"><b>Note</b>  This interface is implemented by the application to handle events that it has subscribed to by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-addactivetextpositionchangedeventhandler">AddActiveTextPositionChangedEventHandler</a>.
			</div>
<div> </div>

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>