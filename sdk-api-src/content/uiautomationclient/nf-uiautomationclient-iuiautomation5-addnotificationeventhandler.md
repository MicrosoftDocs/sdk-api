---
UID: NF:uiautomationclient.IUIAutomation5.AddNotificationEventHandler
title: IUIAutomation5::AddNotificationEventHandler (uiautomationclient.h)
description: Registers a method that handles notification events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
helpviewer_keywords: ["AddNotificationEventHandler","AddNotificationEventHandler method [Windows Accessibility]","AddNotificationEventHandler method [Windows Accessibility]","IUIAutomation5 interface","IUIAutomation5 interface [Windows Accessibility]","AddNotificationEventHandler method","IUIAutomation5.AddNotificationEventHandler","IUIAutomation5::AddNotificationEventHandler","uiautomationclient/IUIAutomation5::AddNotificationEventHandler","winauto.uiauto_IUIAutomation5_AddNotificationEventHandler"]
old-location: winauto\uiauto_IUIAutomation5_AddNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: 1E6A4683-9439-4212-9EA6-91719A515C4B
ms.date: 12/05/2018
ms.keywords: AddNotificationEventHandler, AddNotificationEventHandler method [Windows Accessibility], AddNotificationEventHandler method [Windows Accessibility],IUIAutomation5 interface, IUIAutomation5 interface [Windows Accessibility],AddNotificationEventHandler method, IUIAutomation5.AddNotificationEventHandler, IUIAutomation5::AddNotificationEventHandler, uiautomationclient/IUIAutomation5::AddNotificationEventHandler, winauto.uiauto_IUIAutomation5_AddNotificationEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation5::AddNotificationEventHandler
 - uiautomationclient/IUIAutomation5::AddNotificationEventHandler
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
 - IUIAutomation5.AddNotificationEventHandler
---

# IUIAutomation5::AddNotificationEventHandler


## -description

Registers a method that handles notification events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationnotificationeventhandler">IUIAutomationNotificationEventHandler</a>*</b>

A pointer to the object that handles the notification event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation5">IUIAutomation5</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>