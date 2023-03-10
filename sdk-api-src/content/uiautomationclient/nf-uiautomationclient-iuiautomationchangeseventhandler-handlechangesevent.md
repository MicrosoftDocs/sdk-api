---
UID: NF:uiautomationclient.IUIAutomationChangesEventHandler.HandleChangesEvent
title: IUIAutomationChangesEventHandler::HandleChangesEvent (uiautomationclient.h)
description: Handles one or more Microsoft UI Automation change events.
helpviewer_keywords: ["HandleChangesEvent","HandleChangesEvent method [Windows Accessibility]","HandleChangesEvent method [Windows Accessibility]","IUIAutomationChangesEventHandler interface","IUIAutomationChangesEventHandler interface [Windows Accessibility]","HandleChangesEvent method","IUIAutomationChangesEventHandler.HandleChangesEvent","IUIAutomationChangesEventHandler::HandleChangesEvent","uiautomationclient/IUIAutomationChangesEventHandler::HandleChangesEvent","winauto.uiauto_IUIAutomationChangesEventHandler_HandleChangesEvent"]
old-location: winauto\uiauto_IUIAutomationChangesEventHandler_HandleChangesEvent.htm
tech.root: WinAuto
ms.assetid: 5BCE09F7-9811-49F5-B2C4-8DABC44CA406
ms.date: 12/05/2018
ms.keywords: HandleChangesEvent, HandleChangesEvent method [Windows Accessibility], HandleChangesEvent method [Windows Accessibility],IUIAutomationChangesEventHandler interface, IUIAutomationChangesEventHandler interface [Windows Accessibility],HandleChangesEvent method, IUIAutomationChangesEventHandler.HandleChangesEvent, IUIAutomationChangesEventHandler::HandleChangesEvent, uiautomationclient/IUIAutomationChangesEventHandler::HandleChangesEvent, winauto.uiauto_IUIAutomationChangesEventHandler_HandleChangesEvent
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationChangesEventHandler::HandleChangesEvent
 - uiautomationclient/IUIAutomationChangesEventHandler::HandleChangesEvent
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
 - IUIAutomationChangesEventHandler.HandleChangesEvent
---

# IUIAutomationChangesEventHandler::HandleChangesEvent


## -description

Handles one or more Microsoft UI Automation change events.

## -parameters

### -param sender [in]

A pointer to the element that raised the event.

### -param uiaChanges [in]

A collection of pointers to <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiachangeinfo">UiaChangeInfo</a> structures.

### -param changesCount [in]

The number of changes that occurred. This is the number of <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiachangeinfo">UiaChangeInfo</a> structures pointed to by the <i>uiaChanges</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that it has subscribed to by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-addchangeseventhandler">AddChangesEventHandler</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationchangeseventhandler">IUIAutomationChangesEventHandler</a>