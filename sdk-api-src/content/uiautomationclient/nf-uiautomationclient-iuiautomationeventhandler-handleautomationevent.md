---
UID: NF:uiautomationclient.IUIAutomationEventHandler.HandleAutomationEvent
title: IUIAutomationEventHandler::HandleAutomationEvent (uiautomationclient.h)
description: Handles a Microsoft UI Automation event.
helpviewer_keywords: ["HandleAutomationEvent","HandleAutomationEvent method [Windows Accessibility]","HandleAutomationEvent method [Windows Accessibility]","IUIAutomationEventHandler interface","IUIAutomationEventHandler interface [Windows Accessibility]","HandleAutomationEvent method","IUIAutomationEventHandler.HandleAutomationEvent","IUIAutomationEventHandler::HandleAutomationEvent","uiauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent","uiauto_IUIAutomationEventHandler_HandleAutomationEvent","uiautomationclient/IUIAutomationEventHandler::HandleAutomationEvent","winauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent"]
old-location: winauto\uiauto_IUIAutomationEventHandler_HandleAutomationEvent.htm
tech.root: WinAuto
ms.assetid: 56668923-f21a-4d38-9175-95785892388c
ms.date: 12/05/2018
ms.keywords: HandleAutomationEvent, HandleAutomationEvent method [Windows Accessibility], HandleAutomationEvent method [Windows Accessibility],IUIAutomationEventHandler interface, IUIAutomationEventHandler interface [Windows Accessibility],HandleAutomationEvent method, IUIAutomationEventHandler.HandleAutomationEvent, IUIAutomationEventHandler::HandleAutomationEvent, uiauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent, uiauto_IUIAutomationEventHandler_HandleAutomationEvent, uiautomationclient/IUIAutomationEventHandler::HandleAutomationEvent, winauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationEventHandler::HandleAutomationEvent
 - uiautomationclient/IUIAutomationEventHandler::HandleAutomationEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationEventHandler.HandleAutomationEvent
---

# IUIAutomationEventHandler::HandleAutomationEvent


## -description

Handles a Microsoft UI Automation event.

## -parameters

### -param sender [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to  the element that raised the event.

### -param eventId [in]

Type: <b>EVENTID</b>

The event identifier. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addautomationeventhandler">AddAutomationEventHandler</a>.
			

Adjusting an event handler from within this method is not supported.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandler">IUIAutomationEventHandler</a>