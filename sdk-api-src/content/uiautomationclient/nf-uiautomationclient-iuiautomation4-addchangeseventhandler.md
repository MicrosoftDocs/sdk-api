---
UID: NF:uiautomationclient.IUIAutomation4.AddChangesEventHandler
title: IUIAutomation4::AddChangesEventHandler
author: windows-sdk-content
description: Registers a method that handles change events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
old-location: winauto\uiauto_IUIAutomation4_AddChangesEventHandler.htm
old-project: WinAuto
ms.assetid: E479ACCA-9372-463F-A992-8030E33A2341
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: AddChangesEventHandler, AddChangesEventHandler method [Windows Accessibility], AddChangesEventHandler method [Windows Accessibility],IUIAutomation4 interface, IUIAutomation4 interface [Windows Accessibility],AddChangesEventHandler method, IUIAutomation4.AddChangesEventHandler, IUIAutomation4::AddChangesEventHandler, uiautomationclient/IUIAutomation4::AddChangesEventHandler, winauto.uiauto_IUIAutomation4_AddChangesEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomation4.AddChangesEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation4::AddChangesEventHandler


## -description


Registers a method that handles change events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div><div> </div>

## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.


### -param scope [in]

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


### -param changeTypes [in]

Type: <b>int*</b>

A pointer to a list of integers that indicate the change types the event represents.


### -param changesCount [in]

Type: <b>int</b>

The number of changes that occurred in this event.


### -param pCacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/8DCF8826-B688-416C-9195-34E0290054AA">IUIAutomationChangesEventHandler</a>*</b>

A pointer to the object that handles the changes event.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A Microsoft UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.




## -see-also




<a href="https://msdn.microsoft.com/CA616076-CD04-4753-9605-093C9529C826">IUIAutomation4</a>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>
 

 

