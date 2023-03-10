---
UID: NF:uiautomationclient.IUIAutomation3.RemoveTextEditTextChangedEventHandler
title: IUIAutomation3::RemoveTextEditTextChangedEventHandler (uiautomationclient.h)
description: Removes a programmatic text-edit event handler.
helpviewer_keywords: ["IUIAutomation3 interface [Windows Accessibility]","RemoveTextEditTextChangedEventHandler method","IUIAutomation3.RemoveTextEditTextChangedEventHandler","IUIAutomation3::RemoveTextEditTextChangedEventHandler","RemoveTextEditTextChangedEventHandler","RemoveTextEditTextChangedEventHandler method [Windows Accessibility]","RemoveTextEditTextChangedEventHandler method [Windows Accessibility]","IUIAutomation3 interface","uiautomationclient/IUIAutomation3::RemoveTextEditTextChangedEventHandler","winauto.uiauto_IUIAutomation3_RemoveTextEditTextChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation3_RemoveTextEditTextChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: CCB8C8FC-B0CF-2C3D-64B5-9CCF1BB64058
ms.date: 12/05/2018
ms.keywords: IUIAutomation3 interface [Windows Accessibility],RemoveTextEditTextChangedEventHandler method, IUIAutomation3.RemoveTextEditTextChangedEventHandler, IUIAutomation3::RemoveTextEditTextChangedEventHandler, RemoveTextEditTextChangedEventHandler, RemoveTextEditTextChangedEventHandler method [Windows Accessibility], RemoveTextEditTextChangedEventHandler method [Windows Accessibility],IUIAutomation3 interface, uiautomationclient/IUIAutomation3::RemoveTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomation3_RemoveTextEditTextChangedEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IUIAutomation3::RemoveTextEditTextChangedEventHandler
 - uiautomationclient/IUIAutomation3::RemoveTextEditTextChangedEventHandler
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
 - IUIAutomation3.RemoveTextEditTextChangedEventHandler
---

# IUIAutomation3::RemoveTextEditTextChangedEventHandler


## -description

Removes a programmatic text-edit event handler.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler">IUIAutomationTextEditTextChangedEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation3-addtextedittextchangedeventhandler">IUIAutomation3::AddTextEditTextChangedEventHandler</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A Microsoft UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, 
if the event is received simultaneously with the request to unsubscribe the event. The best practice 
is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count 
has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an 
access violation if an event is delivered late.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation3">IUIAutomation3</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>