---
UID: NF:uiautomationclient.IUIAutomationChangesEventHandler.HandleChangesEvent
title: IUIAutomationChangesEventHandler::HandleChangesEvent
author: windows-sdk-content
description: Handles a Microsoft UI Automation changes event.
old-location: winauto\uiauto_IUIAutomationChangesEventHandler_HandleChangesEvent.htm
tech.root: WinAuto
ms.assetid: 5BCE09F7-9811-49F5-B2C4-8DABC44CA406
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HandleChangesEvent, HandleChangesEvent method [Windows Accessibility], HandleChangesEvent method [Windows Accessibility],IUIAutomationChangesEventHandler interface, IUIAutomationChangesEventHandler interface [Windows Accessibility],HandleChangesEvent method, IUIAutomationChangesEventHandler.HandleChangesEvent, IUIAutomationChangesEventHandler::HandleChangesEvent, uiautomationclient/IUIAutomationChangesEventHandler::HandleChangesEvent, winauto.uiauto_IUIAutomationChangesEventHandler_HandleChangesEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
 - IUIAutomationChangesEventHandler.HandleChangesEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationChangesEventHandler::HandleChangesEvent


## -description


Handles a Microsoft UI Automation changes event.


## -parameters




### -param sender [in]

A pointer to the element that raised the event.


### -param uiaChanges [in]

A collection of pointers to <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures.


### -param changesCount [in]

The number of changes that occurred. This is the number of <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures pointed to by the <i>uiaChanges</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by calling <a href="https://msdn.microsoft.com/E479ACCA-9372-463F-A992-8030E33A2341">AddChangesEventHandler</a>.




## -see-also




<a href="https://msdn.microsoft.com/8DCF8826-B688-416C-9195-34E0290054AA">IUIAutomationChangesEventHandler</a>
 

 

