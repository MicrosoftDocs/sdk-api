---
UID: NF:uiautomationclient.IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent
title: IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent (uiautomationclient.h)
description: Handles a Microsoft UI Automation property-changed event.
helpviewer_keywords: ["HandlePropertyChangedEvent","HandlePropertyChangedEvent method [Windows Accessibility]","HandlePropertyChangedEvent method [Windows Accessibility]","IUIAutomationPropertyChangedEventHandler interface","IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility]","HandlePropertyChangedEvent method","IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent","IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent","uiauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent","uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent","uiautomationclient/IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent","winauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent"]
old-location: winauto\uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent.htm
tech.root: WinAuto
ms.assetid: 3b0bb9a0-b2a5-4843-9431-cc00e1836dd1
ms.date: 12/05/2018
ms.keywords: HandlePropertyChangedEvent, HandlePropertyChangedEvent method [Windows Accessibility], HandlePropertyChangedEvent method [Windows Accessibility],IUIAutomationPropertyChangedEventHandler interface, IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility],HandlePropertyChangedEvent method, IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent, IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent, uiauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent, uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent, uiautomationclient/IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent, winauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent
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
 - IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent
 - uiautomationclient/IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent
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
 - IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent
---

# IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent


## -description

Handles a Microsoft UI Automation property-changed event.

## -parameters

### -param sender [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property whose value has changed. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param newValue [in]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a></b>

The new property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">AddPropertyChangedEventHandler</a>.
			

Adjusting an event handler from within this method is not supported.