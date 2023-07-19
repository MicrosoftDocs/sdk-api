---
UID: NF:uiautomationclient.IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
title: IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent (uiautomationclient.h)
description: Handles an event that is raised when a Microsoft UI Automation provider for a text-edit control reports a programmatic text change.
helpviewer_keywords: ["HandleTextEditTextChangedEvent","HandleTextEditTextChangedEvent method [Windows Accessibility]","HandleTextEditTextChangedEvent method [Windows Accessibility]","IUIAutomationTextEditTextChangedEventHandler interface","IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility]","HandleTextEditTextChangedEvent method","IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent","IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent","uiautomationclient/IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent","winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler_HandleTextEditTextChangedEvent"]
old-location: winauto\uiauto_IUIAutomationTextEditTextChangedEventHandler_HandleTextEditTextChangedEvent.htm
tech.root: WinAuto
ms.assetid: FA63086A-40C5-BE7B-DC4E-2C8547636AE8
ms.date: 12/05/2018
ms.keywords: HandleTextEditTextChangedEvent, HandleTextEditTextChangedEvent method [Windows Accessibility], HandleTextEditTextChangedEvent method [Windows Accessibility],IUIAutomationTextEditTextChangedEventHandler interface, IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility],HandleTextEditTextChangedEvent method, IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent, IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent, uiautomationclient/IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent, winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler_HandleTextEditTextChangedEvent
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
 - IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent
 - uiautomationclient/IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent
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
 - IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
---

# IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent


## -description

Handles an event that is raised when a Microsoft UI Automation provider for a text-edit control reports a programmatic text change.

## -parameters

### -param sender [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.

### -param textEditChangeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a></b>

The type of text-edit change that occurred.

### -param eventStrings [in]

Type: <b><a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">SAFEARRAY</a>*</b>

Event data passed by the event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the application to handle events that it has subscribed to by using <b>AddTextEditTextChangedEventHandler</b>.

The event data contains different payloads for each text-edit change type:

<ul>
<li><b>TextEditChangeType_AutoCorrect</b>: Data is the new corrected string .</li>
<li><b>TextEditChangeType_Composition</b>: Data is the updated string in the composition (only the part that changed).</li>
<li><b>TextEditChangeType_CompositionFinalized</b>: Data is the finalized string of the completed composition (this may be empty if composition was canceled or deleted).</li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler">IUIAutomationTextEditTextChangedEventHandler</a>