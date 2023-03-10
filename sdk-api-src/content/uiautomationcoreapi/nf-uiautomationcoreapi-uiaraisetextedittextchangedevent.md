---
UID: NF:uiautomationcoreapi.UiaRaiseTextEditTextChangedEvent
title: UiaRaiseTextEditTextChangedEvent function (uiautomationcoreapi.h)
description: Called by a provider to notify the Microsoft UI Automation core that a text control has programmatically changed text. (UiaRaiseTextEditTextChangedEvent)
helpviewer_keywords: ["UiaRaiseTextEditTextChangedEvent","UiaRaiseTextEditTextChangedEvent function [Windows Accessibility]","uiautomationcoreapi/UiaRaiseTextEditTextChangedEvent","winauto.uiauto_UiaRaiseTextEditTextChangedEventFunction"]
old-location: winauto\uiauto_UiaRaiseTextEditTextChangedEventFunction.htm
tech.root: WinAuto
ms.assetid: 19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819
ms.date: 09/24/2020
ms.keywords: UiaRaiseTextEditTextChangedEvent, UiaRaiseTextEditTextChangedEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseTextEditTextChangedEvent, winauto.uiauto_UiaRaiseTextEditTextChangedEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - UiaRaiseTextEditTextChangedEvent
 - uiautomationcoreapi/UiaRaiseTextEditTextChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseTextEditTextChangedEvent
---

# UiaRaiseTextEditTextChangedEvent function

## -description

Called by a provider to notify the Microsoft UI Automation core that a text control has programmatically changed text.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider node where the text change occurred.

### -param textEditChangeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a></b>

The type of text-edit change that occurred.

### -param pChangedData [in]

Type: <b><a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">SAFEARRAY</a>*</b>

The event data. Should be assignable as a <b>VAR</b> of type <b>VT_BSTR</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is a helper function for providers that implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider">ITextEditProvider</a> and are raising the pattern's required events. Follow the guidance given in <a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a> that describes when to raise the events and what payload the events should pass to UI Automation.

If there are no clients listening for a particular change type, no event is raised.

The event data should contain different payloads for each change type (per <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a>):

<ul>
<li><b>TextEditChangeType_AutoCorrect</b>: <i>pChangedData</i> should be the new corrected string .</li>
<li><b>TextEditChangeType_Composition</b>: <i>pChangedData</i> should be the updated string in the composition (only the part that changed).</li>
<li><b>TextEditChangeType_CompositionFinalized</b>: <i>pChangedData</i> should be the finalized string of the completed composition (this may be empty if composition was canceled or deleted).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextedittextchangedeventhandler-handletextedittextchangedevent">HandleTextEditTextChangedEvent</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider">ITextEditProvider</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation3-addtextedittextchangedeventhandler">IUIAutomation3::AddTextEditTextChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a>
