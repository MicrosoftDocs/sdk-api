---
UID: NF:uiautomationclient.IUIAutomation5.RemoveNotificationEventHandler
title: IUIAutomation5::RemoveNotificationEventHandler (uiautomationclient.h)
description: Removes a notification event handler.
helpviewer_keywords: ["IUIAutomation5 interface [Windows Accessibility]","RemoveNotificationEventHandler method","IUIAutomation5.RemoveNotificationEventHandler","IUIAutomation5::RemoveNotificationEventHandler","RemoveNotificationEventHandler","RemoveNotificationEventHandler method [Windows Accessibility]","RemoveNotificationEventHandler method [Windows Accessibility]","IUIAutomation5 interface","uiautomationclient/IUIAutomation5::RemoveNotificationEventHandler","winauto.uiauto_IUIAutomation5_RemoveNotificationEventHandler"]
old-location: winauto\uiauto_IUIAutomation5_RemoveNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: E0775AB3-814F-4420-9764-333572DAD201
ms.date: 12/05/2018
ms.keywords: IUIAutomation5 interface [Windows Accessibility],RemoveNotificationEventHandler method, IUIAutomation5.RemoveNotificationEventHandler, IUIAutomation5::RemoveNotificationEventHandler, RemoveNotificationEventHandler, RemoveNotificationEventHandler method [Windows Accessibility], RemoveNotificationEventHandler method [Windows Accessibility],IUIAutomation5 interface, uiautomationclient/IUIAutomation5::RemoveNotificationEventHandler, winauto.uiauto_IUIAutomation5_RemoveNotificationEventHandler
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
 - IUIAutomation5::RemoveNotificationEventHandler
 - uiautomationclient/IUIAutomation5::RemoveNotificationEventHandler
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
 - IUIAutomation5.RemoveNotificationEventHandler
---

# IUIAutomation5::RemoveNotificationEventHandler


## -description

Removes a notification event handler.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationnotificationeventhandler">IUIAutomationNotificationEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler">AddNotificationEventHandler</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation5">IUIAutomation5</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>