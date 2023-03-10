---
UID: NF:uiautomationclient.IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent
title: IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent (uiautomationclient.h)
description: Handles the event raised when the keyboard focus moves to a different UI Automation element.
helpviewer_keywords: ["HandleFocusChangedEvent","HandleFocusChangedEvent method [Windows Accessibility]","HandleFocusChangedEvent method [Windows Accessibility]","IUIAutomationFocusChangedEventHandler interface","IUIAutomationFocusChangedEventHandler interface [Windows Accessibility]","HandleFocusChangedEvent method","IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent","IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent","uiauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent","uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent","uiautomationclient/IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent","winauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent"]
old-location: winauto\uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent.htm
tech.root: WinAuto
ms.assetid: 7d90982f-4805-4ebb-a9f9-e335dc15d519
ms.date: 12/05/2018
ms.keywords: HandleFocusChangedEvent, HandleFocusChangedEvent method [Windows Accessibility], HandleFocusChangedEvent method [Windows Accessibility],IUIAutomationFocusChangedEventHandler interface, IUIAutomationFocusChangedEventHandler interface [Windows Accessibility],HandleFocusChangedEvent method, IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent, IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent, uiauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent, uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent, uiautomationclient/IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent, winauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent
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
 - IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent
 - uiautomationclient/IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent
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
 - IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent
---

# IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent


## -description

Handles the event raised when the keyboard focus moves to a different UI Automation element.

## -parameters

### -param sender [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element that has received the focus.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that were subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler">AddFocusChangedEventHandler</a>


The UI Automation element represented by <i>sender</i> might not have any cached properties or control patterns, depending on whether the application subscribed to this event while a cache request was active.

Adjusting an event handler from within this method is not supported.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler">IUIAutomationFocusChangedEventHandler</a>