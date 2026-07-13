---
UID: NF:uiautomationcoreapi.UiaRaiseAutomationEvent
title: UiaRaiseAutomationEvent function (uiautomationcoreapi.h)
description: Notifies listeners of an event.
helpviewer_keywords: ["UiaRaiseAutomationEvent","UiaRaiseAutomationEvent function [Windows Accessibility]","uiauto.uiauto_UiaRaiseAutomationEventFunction","uiauto_UiaRaiseAutomationEventFunction","uiautomationcoreapi/UiaRaiseAutomationEvent","winauto.uiauto_UiaRaiseAutomationEventFunction"]
old-location: winauto\uiauto_UiaRaiseAutomationEventFunction.htm
tech.root: WinAuto
ms.assetid: a91ce84c-faae-4b8b-9547-9e9d8edbde6e
ms.date: 12/05/2018
ms.keywords: UiaRaiseAutomationEvent, UiaRaiseAutomationEvent function [Windows Accessibility], uiauto.uiauto_UiaRaiseAutomationEventFunction, uiauto_UiaRaiseAutomationEventFunction, uiautomationcoreapi/UiaRaiseAutomationEvent, winauto.uiauto_UiaRaiseAutomationEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaRaiseAutomationEvent
 - uiautomationcoreapi/UiaRaiseAutomationEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseAutomationEvent
---

# UiaRaiseAutomationEvent function


## -description

Notifies listeners of an event.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider element where the event occurred.

### -param id [in]

Type: <b>EVENTID</b>

The identifier of the event to be raised. For a list of event IDs, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function increments the reference counter of the <i>pProvider</i> interface, and UI Automation decrements the reference counter when the event handers finish processing the event.