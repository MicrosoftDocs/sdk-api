---
UID: NF:uiautomationclient.IUIAutomation3.AddTextEditTextChangedEventHandler
title: IUIAutomation3::AddTextEditTextChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles programmatic text-edit events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
old-location: winauto\uiauto_IUIAutomation3_AddTextEditTextChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: E4FBD04E-2E0B-6B87-F589-C3214EF54E5F
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddTextEditTextChangedEventHandler, AddTextEditTextChangedEventHandler method [Windows Accessibility], AddTextEditTextChangedEventHandler method [Windows Accessibility],IUIAutomation3 interface, IUIAutomation3 interface [Windows Accessibility],AddTextEditTextChangedEventHandler method, IUIAutomation3.AddTextEditTextChangedEventHandler, IUIAutomation3::AddTextEditTextChangedEventHandler, uiautomationclient/IUIAutomation3::AddTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomation3_AddTextEditTextChangedEventHandler
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
 - IUIAutomation3.AddTextEditTextChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation3::AddTextEditTextChangedEventHandler


## -description


Registers a method that handles programmatic text-edit events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div><div> </div>

## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.


### -param arg1

TBD


### -param arg2 [in]

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/1308F513-5458-900C-A494-9AC9131C2D1E">IUIAutomationTextEditTextChangedEventHandler</a>*</b>

A pointer to the object that handles the programmatic text-edit event.



#### - arg3 [in]

Type: <b><a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a></b>

The specific change type to listen for. Clients register for each text-edit change type separately, so that the UI Automation system can check for registered listeners at run-time and avoid raising events for particular text-edit changes when there are no listeners.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.




## -see-also




<a href="https://msdn.microsoft.com/948b3bb9-75a9-4197-9680-e6fe7bb86feb">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/D46CE3FF-31E2-32CE-FD38-680064E1765D">IUIAutomation3</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>



<a href="https://msdn.microsoft.com/b0f8bb2a-003f-471f-b1a6-ffec97e2752a">RemoveTextEditTextChangedEventHandler</a>



<a href="https://msdn.microsoft.com/7019ecb8-6123-4e00-926c-6725d7e71385">Subscribing to UI Automation Events</a>



<a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>
 

 

