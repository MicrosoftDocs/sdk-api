---
UID: NF:uiautomationclient.IUIAutomationActiveTextPositionChangedEventHandler.HandleActiveTextPositionChangedEvent
title: IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent (uiautomationclient.h)
description: Handles a Microsoft UI Automation active text position change event.
helpviewer_keywords: ["HandleActiveTextPositionChangedEvent","HandleActiveTextPositionChangedEvent method [Windows Accessibility]","HandleActiveTextPositionChangedEvent method [Windows Accessibility]","IUIAutomationActiveTextPositionChangedEventHandler interface","IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility]","HandleActiveTextPositionChangedEvent method","IUIAutomationActiveTextPositionChangedEventHandler.HandleActiveTextPositionChangedEvent","IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent","uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent","winauto.uiauto_IUIAutomationActiveTextPositionChangedEventHandler_HandleActiveTextPositionChangedEvent"]
old-location: winauto\uiauto_IUIAutomationActiveTextPositionChangedEventHandler_HandleActiveTextPositionChangedEvent.htm
tech.root: WinAuto
ms.assetid: 8A33EDF1-A518-4701-A160-71B5A998CC00
ms.date: 12/05/2018
ms.keywords: HandleActiveTextPositionChangedEvent, HandleActiveTextPositionChangedEvent method [Windows Accessibility], HandleActiveTextPositionChangedEvent method [Windows Accessibility],IUIAutomationActiveTextPositionChangedEventHandler interface, IUIAutomationActiveTextPositionChangedEventHandler interface [Windows Accessibility],HandleActiveTextPositionChangedEvent method, IUIAutomationActiveTextPositionChangedEventHandler.HandleActiveTextPositionChangedEvent, IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent, uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent, winauto.uiauto_IUIAutomationActiveTextPositionChangedEventHandler_HandleActiveTextPositionChangedEvent
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
 - IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent
 - uiautomationclient/IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent
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
 - IUIAutomationActiveTextPositionChangedEventHandler.HandleActiveTextPositionChangedEvent
---

# IUIAutomationActiveTextPositionChangedEventHandler::HandleActiveTextPositionChangedEvent


## -description

Handles a Microsoft UI Automation active text position change event.<div class="alert"><b>Note</b>  This method is implemented by the application to handle events that it has subscribed to by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-addactivetextpositionchangedeventhandler">AddActiveTextPositionChangedEventHandler</a>.</div>
<div> </div>

## -parameters

### -param sender [in]

A pointer to the UI Automation element that raised the event.

### -param range

A span of continuous text in a container that supports the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.

## -see-also

<a href="../uiautomationclient/nn-uiautomationclient-iuiautomationactivetextpositionchangedeventhandler.md">IUIAutomationActiveTextPositionChangedEventHandler</a>
