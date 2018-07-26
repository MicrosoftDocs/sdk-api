---
UID: NF:uiautomationcoreapi.UiaRaiseTextEditTextChangedEvent
title: UiaRaiseTextEditTextChangedEvent function
author: windows-sdk-content
description: Called by a provider to notify the Microsoft UI Automation core that a text control has programmatically changed text.
old-location: winauto\uiauto_UiaRaiseTextEditTextChangedEventFunction.htm
old-project: WinAuto
ms.assetid: 19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: UiaRaiseTextEditTextChangedEvent, UiaRaiseTextEditTextChangedEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseTextEditTextChangedEvent, winauto.uiauto_UiaRaiseTextEditTextChangedEventFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaRaiseTextEditTextChangedEvent function


## -description


Called by a provider to notify the Microsoft UI Automation core that a text control has programmatically changed text.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the text change occurred.


### -param textEditChangeType [in]

Type: <b><a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a></b>

The type of text-edit change that occurred.


### -param pChangedData [in]

Type: <b><a href="uiauto_WorkingWithSafeArrays.htm">SAFEARRAY</a>*</b>

The event data. Should be assignable as a <b>VAR</b> of type <b>VT_BSTR</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is a helper function for providers that implement <a href="https://msdn.microsoft.com/6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326">ITextEditProvider</a> and are raising the pattern's required events. Follow the guidance given in <a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a> that describes when to raise the events and what payload the events should pass to UI Automation.

If there are no clients listening for a particular change type, no event is raised.

The event data should contain different payloads for each change type (per <a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a>):

<ul>
<li><b>TextEditChangeType_AutoCorrect</b>: <i>pChangedData</i> should be the new corrected string .</li>
<li><b>TextEditChangeType_Composition</b>: <i>pChangedData</i> should be the updated string in the composition (only the part that changed).</li>
<li><b>TextEditChangeType_CompositionFinalized</b>: <i>pChangedData</i> should be the finalized string of the completed composition (this may be empty if composition was canceled or deleted).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/FA63086A-40C5-BE7B-DC4E-2C8547636AE8">HandleTextEditTextChangedEvent</a>



<a href="https://msdn.microsoft.com/6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326">ITextEditProvider</a>



<a href="https://msdn.microsoft.com/E4FBD04E-2E0B-6B87-F589-C3214EF54E5F">IUIAutomation3::AddTextEditTextChangedEventHandler</a>



<a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a>
 

 

