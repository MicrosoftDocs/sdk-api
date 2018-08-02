---
UID: NF:uiautomationclient.IUIAutomation5.AddNotificationEventHandler
title: IUIAutomation5::AddNotificationEventHandler
author: windows-sdk-content
description: Registers a method that handles notification events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
old-location: winauto\uiauto_IUIAutomation5_AddNotificationEventHandler.htm
old-project: WinAuto
ms.assetid: 1E6A4683-9439-4212-9EA6-91719A515C4B
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AddNotificationEventHandler, AddNotificationEventHandler method [Windows Accessibility], AddNotificationEventHandler method [Windows Accessibility],IUIAutomation5 interface, IUIAutomation5 interface [Windows Accessibility],AddNotificationEventHandler method, IUIAutomation5.AddNotificationEventHandler, IUIAutomation5::AddNotificationEventHandler, uiautomationclient/IUIAutomation5::AddNotificationEventHandler, winauto.uiauto_IUIAutomation5_AddNotificationEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation5.AddNotificationEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation5::AddNotificationEventHandler


## -description


Registers a method that handles notification events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div><div> </div>

## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.


### -param scope [in]

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/7E12B8C2-D6A7-4637-9049-312B78EC01DE">IUIAutomationNotificationEventHandler</a>*</b>

A pointer to the object that handles the notification event.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BCF67DB0-DF5B-4CED-9C32-01F126494129">IUIAutomation5</a>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>
 

 

