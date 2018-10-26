---
UID: NF:uiautomationclient.IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
title: IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent
author: windows-sdk-content
description: Handles an event that is raised when a Microsoft UI Automation provider for a text-edit control reports a programmatic text change.
old-location: winauto\uiauto_IUIAutomationTextEditTextChangedEventHandler_HandleTextEditTextChangedEvent.htm
tech.root: WinAuto
ms.assetid: FA63086A-40C5-BE7B-DC4E-2C8547636AE8
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: HandleTextEditTextChangedEvent, HandleTextEditTextChangedEvent method [Windows Accessibility], HandleTextEditTextChangedEvent method [Windows Accessibility],IUIAutomationTextEditTextChangedEventHandler interface, IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility],HandleTextEditTextChangedEvent method, IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent, IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent, uiautomationclient/IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent, winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler_HandleTextEditTextChangedEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent


## -description


Handles an event that is raised when a Microsoft UI Automation provider for a text-edit control reports a programmatic text change.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.


### -param arg1

TBD


### -param eventStrings [in]

Type: <b><a href="uiauto_WorkingWithSafeArrays.htm">SAFEARRAY</a>*</b>

Event data passed by the event.


#### - textEditChangeType [in]

Type: <b><a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a></b>

The type of text-edit change that occurred.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by using <b>AddTextEditTextChangedEventHandler</b>.

The event data contains different payloads for each text-edit change type:

<ul>
<li><b>TextEditChangeType_AutoCorrect</b>: Data is the new corrected string .</li>
<li><b>TextEditChangeType_Composition</b>: Data is the updated string in the composition (only the part that changed).</li>
<li><b>TextEditChangeType_CompositionFinalized</b>: Data is the finalized string of the completed composition (this may be empty if composition was canceled or deleted).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/1308F513-5458-900C-A494-9AC9131C2D1E">IUIAutomationTextEditTextChangedEventHandler</a>
 

 

