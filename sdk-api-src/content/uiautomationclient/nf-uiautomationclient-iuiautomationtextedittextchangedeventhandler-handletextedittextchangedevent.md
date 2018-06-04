---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAutomationTextEditTextChangedEventHandler::HandleTextEditTextChangedEvent


## -description


Handles an event that is raised when a Microsoft UI Automation provider for a text-edit control reports a programmatic text change.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.


### -param textEditChangeType [in]

Type: <b><a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a></b>

The type of text-edit change that occurred.


### -param eventStrings [in]

Type: <b><a href="uiauto_WorkingWithSafeArrays.htm">SAFEARRAY</a>*</b>

Event data passed by the event.


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
 

 

