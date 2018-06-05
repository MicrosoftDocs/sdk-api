---
UID: NF:uiautomationclient.IUIAutomation3.RemoveTextEditTextChangedEventHandler
title: IUIAutomation3::RemoveTextEditTextChangedEventHandler
author: windows-sdk-content
description: Removes a programmatic text-edit event handler.
old-location: winauto\uiauto_IUIAutomation3_RemoveTextEditTextChangedEventHandler.htm
old-project: WinAuto
ms.assetid: CCB8C8FC-B0CF-2C3D-64B5-9CCF1BB64058
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomation3 interface [Windows Accessibility],RemoveTextEditTextChangedEventHandler method, IUIAutomation3.RemoveTextEditTextChangedEventHandler, IUIAutomation3::RemoveTextEditTextChangedEventHandler, RemoveTextEditTextChangedEventHandler, RemoveTextEditTextChangedEventHandler method [Windows Accessibility], RemoveTextEditTextChangedEventHandler method [Windows Accessibility],IUIAutomation3 interface, uiautomationclient/IUIAutomation3::RemoveTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomation3_RemoveTextEditTextChangedEventHandler
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomation3.RemoveTextEditTextChangedEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation3::RemoveTextEditTextChangedEventHandler


## -description


Removes a programmatic text-edit event handler.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/1308F513-5458-900C-A494-9AC9131C2D1E">IUIAutomationTextEditTextChangedEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="https://msdn.microsoft.com/E4FBD04E-2E0B-6B87-F589-C3214EF54E5F">IUIAutomation3::AddTextEditTextChangedEventHandler</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A Microsoft UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, 
if the event is received simultaneously with the request to unsubscribe the event. The best practice 
is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count 
has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an 
access violation if an event is delivered late.




## -see-also




<a href="https://msdn.microsoft.com/D46CE3FF-31E2-32CE-FD38-680064E1765D">IUIAutomation3</a>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>
 

 

