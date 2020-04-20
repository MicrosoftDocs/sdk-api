---
UID: NF:uiautomationclient.IUIAutomation6.put_CoalesceEvents
title: IUIAutomation6::put_CoalesceEvents (uiautomationclient.h)
description: Gets or sets whether an accessible technology client receives all events, or a subset where duplicate events are detected and filtered.helpviewer_keywords: ["CoalesceEvents property [Windows Accessibility]","CoalesceEvents property [Windows Accessibility]","IUIAutomation6 interface","IUIAutomation6 interface [Windows Accessibility]","CoalesceEvents property","IUIAutomation6.CoalesceEvents","IUIAutomation6.put_CoalesceEvents","IUIAutomation6::CoalesceEvents","IUIAutomation6::get_CoalesceEvents","IUIAutomation6::put_CoalesceEvents","put_CoalesceEvents","uiautomationclient/IUIAutomation6::CoalesceEvents","uiautomationclient/IUIAutomation6::get_CoalesceEvents","uiautomationclient/IUIAutomation6::put_CoalesceEvents","winauto.uiauto_IUIAutomation6_CoalesceEvents"]
old-location: winauto\uiauto_IUIAutomation6_CoalesceEvents.htm
tech.root: WinAuto
ms.assetid: 44BBBE06-6A41-4DE7-8C1B-E277D3FCB545
ms.date: 12/05/2019
ms.keywords: CoalesceEvents property [Windows Accessibility], CoalesceEvents property [Windows Accessibility],IUIAutomation6 interface, IUIAutomation6 interface [Windows Accessibility],CoalesceEvents property, IUIAutomation6.CoalesceEvents, IUIAutomation6.put_CoalesceEvents, IUIAutomation6::CoalesceEvents, IUIAutomation6::get_CoalesceEvents, IUIAutomation6::put_CoalesceEvents, put_CoalesceEvents, uiautomationclient/IUIAutomation6::CoalesceEvents, uiautomationclient/IUIAutomation6::get_CoalesceEvents, uiautomationclient/IUIAutomation6::put_CoalesceEvents, winauto.uiauto_IUIAutomation6_CoalesceEvents
f1_keywords:
- uiautomationclient/IUIAutomation6.CoalesceEvents
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomation6.CoalesceEvents
- IUIAutomation6.get_CoalesceEvents
- IUIAutomation6.put_CoalesceEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# IUIAutomation6::put_CoalesceEvents

## -description

Gets or sets whether an accessible technology client receives all events, or a subset where duplicate events are detected and filtered.

This property is read/write.

## -remarks

> ### Parameters
>
> `coalesceEventsOptions` [out]
>
> Type: **CoalesceEventsOptions**
>
> Value indicating whether events are filtered. The default is [CoalesceEventsOptions_Disabled](ne-uiautomationclient-coalesceeventsoptions.md).

## -see-also

[IUIAutomation6 interface](nn-uiautomationclient-iuiautomation6.md)
