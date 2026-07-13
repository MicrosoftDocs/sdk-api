---
UID: NF:uiautomationclient.IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent
title: IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent (uiautomationclient.h)
description: Handles an event that is raised when the Microsoft UI Automation tree structure has changed.
helpviewer_keywords: ["HandleStructureChangedEvent","HandleStructureChangedEvent method [Windows Accessibility]","HandleStructureChangedEvent method [Windows Accessibility]","IUIAutomationStructureChangedEventHandler interface","IUIAutomationStructureChangedEventHandler interface [Windows Accessibility]","HandleStructureChangedEvent method","IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent","IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent","uiauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent","uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent","uiautomationclient/IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent","winauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent"]
old-location: winauto\uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent.htm
tech.root: WinAuto
ms.assetid: 0fdaf2d3-cfd1-4c93-a7cd-94ec83b3e812
ms.date: 12/05/2018
ms.keywords: HandleStructureChangedEvent, HandleStructureChangedEvent method [Windows Accessibility], HandleStructureChangedEvent method [Windows Accessibility],IUIAutomationStructureChangedEventHandler interface, IUIAutomationStructureChangedEventHandler interface [Windows Accessibility],HandleStructureChangedEvent method, IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent, IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent, uiauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent, uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent, uiautomationclient/IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent, winauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent
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
 - IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent
 - uiautomationclient/IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent
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
 - IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent
---

# IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent


## -description

Handles an event that is raised when the Microsoft UI Automation tree structure has changed.

## -parameters

### -param sender [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.

### -param changeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType</a></b>

A value indicating the type of tree structure change that took place.

### -param runtimeId [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

Receives the runtime identifier of the element. This parameter is used only when <i>changeType</i> is <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType_ChildRemoved</a>; it is <b>NULL</b> for all other structure-change events.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler">AddStructureChangedEventHandler</a>


Adjusting an event handler from within this method is not supported.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler">IUIAutomationStructureChangedEventHandler</a>