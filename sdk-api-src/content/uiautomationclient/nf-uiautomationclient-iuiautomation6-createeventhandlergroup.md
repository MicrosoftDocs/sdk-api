---
UID: NF:uiautomationclient.IUIAutomation6.CreateEventHandlerGroup
title: IUIAutomation6::CreateEventHandlerGroup (uiautomationclient.h)
description: Registers one or more event listeners in a single method call.
helpviewer_keywords: ["CreateEventHandlerGroup","CreateEventHandlerGroup method [Windows Accessibility]","CreateEventHandlerGroup method [Windows Accessibility]","IUIAutomation6 interface","IUIAutomation6 interface [Windows Accessibility]","CreateEventHandlerGroup method","IUIAutomation6.CreateEventHandlerGroup","IUIAutomation6::CreateEventHandlerGroup","uiautomationclient/IUIAutomation6::CreateEventHandlerGroup","winauto.uiauto_IUIAutomation6_CreateEventHandlerGroup"]
old-location: winauto\uiauto_IUIAutomation6_CreateEventHandlerGroup.htm
tech.root: WinAuto
ms.assetid: C15C5099-B409-4F75-B6BB-D3ECFBE0B762
ms.date: 12/05/2019
ms.keywords: CreateEventHandlerGroup, CreateEventHandlerGroup method [Windows Accessibility], CreateEventHandlerGroup method [Windows Accessibility],IUIAutomation6 interface, IUIAutomation6 interface [Windows Accessibility],CreateEventHandlerGroup method, IUIAutomation6.CreateEventHandlerGroup, IUIAutomation6::CreateEventHandlerGroup, uiautomationclient/IUIAutomation6::CreateEventHandlerGroup, winauto.uiauto_IUIAutomation6_CreateEventHandlerGroup
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
 - IUIAutomation6::CreateEventHandlerGroup
 - uiautomationclient/IUIAutomation6::CreateEventHandlerGroup
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
 - IUIAutomation6.CreateEventHandlerGroup
---

# IUIAutomation6::CreateEventHandlerGroup


## -description

Registers one or more event listeners in a single method call.

> [!Important]
> Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various [IUIAutomation interface](nn-uiautomationclient-iuiautomation.md).

## -parameters

### -param handlerGroup [out]

A collection of UI Automation event listeners.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in [Understanding Threading Issues](/windows/desktop/WinAuto/uiauto-threading).

## -see-also

[AddEventHandlerGroup](nf-uiautomationclient-iuiautomation6-addeventhandlergroup.md), [IUIAutomation6 interface](nn-uiautomationclient-iuiautomation6.md), [IUIAutomation6::RemoveEventHandlerGroup](nf-uiautomationclient-iuiautomation6-removeeventhandlergroup.md)