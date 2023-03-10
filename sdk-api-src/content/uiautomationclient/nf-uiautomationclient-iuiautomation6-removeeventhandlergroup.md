---
UID: NF:uiautomationclient.IUIAutomation6.RemoveEventHandlerGroup
title: IUIAutomation6::RemoveEventHandlerGroup (uiautomationclient.h)
description: Asynchronously removes the specified UI Automation event handler group.
helpviewer_keywords: ["IUIAutomation6 interface [Windows Accessibility]","RemoveEventHandlerGroup method","IUIAutomation6.RemoveEventHandlerGroup","IUIAutomation6::RemoveEventHandlerGroup","RemoveEventHandlerGroup","RemoveEventHandlerGroup method [Windows Accessibility]","RemoveEventHandlerGroup method [Windows Accessibility]","IUIAutomation6 interface","uiautomationclient/IUIAutomation6::RemoveEventHandlerGroup","winauto.uiauto_IUIAutomation6_RemoveEventHandlerGroup"]
old-location: winauto\uiauto_IUIAutomation6_RemoveEventHandlerGroup.htm
tech.root: WinAuto
ms.assetid: 43BDE7F5-67DF-4DE5-AEDE-068421375E07
ms.date: 12/05/2019
ms.keywords: IUIAutomation6 interface [Windows Accessibility],RemoveEventHandlerGroup method, IUIAutomation6.RemoveEventHandlerGroup, IUIAutomation6::RemoveEventHandlerGroup, RemoveEventHandlerGroup, RemoveEventHandlerGroup method [Windows Accessibility], RemoveEventHandlerGroup method [Windows Accessibility],IUIAutomation6 interface, uiautomationclient/IUIAutomation6::RemoveEventHandlerGroup, winauto.uiauto_IUIAutomation6_RemoveEventHandlerGroup
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - IUIAutomation6::RemoveEventHandlerGroup
 - uiautomationclient/IUIAutomation6::RemoveEventHandlerGroup
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
 - IUIAutomation6.RemoveEventHandlerGroup
---

# IUIAutomation6::RemoveEventHandlerGroup


## -description

Asynchronously removes the specified UI Automation event handler group.

## -parameters

### -param element [in]

A pointer to the UI Automation element associated with the event handler group.

### -param handlerGroup

A collection of UI Automation event listeners.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in [Understanding Threading Issues](/windows/desktop/WinAuto/uiauto-threading).

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, if the event is received simultaneously with the request to unsubscribe the event. The best practice is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an access violation if an event is delivered late.

## -see-also

[IUIAutomation6::AddEventHandlerGroup](nf-uiautomationclient-iuiautomation6-addeventhandlergroup.md), [IUIAutomation6 interface](nn-uiautomationclient-iuiautomation6.md)