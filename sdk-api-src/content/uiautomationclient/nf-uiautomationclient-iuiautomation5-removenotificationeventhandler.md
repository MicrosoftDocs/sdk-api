---
UID: NF:uiautomationclient.IUIAutomation5.RemoveNotificationEventHandler
title: IUIAutomation5::RemoveNotificationEventHandler
author: windows-sdk-content
description: Removes a notification event handler.
old-location: winauto\uiauto_IUIAutomation5_RemoveNotificationEventHandler.htm
tech.root: WinAuto
ms.assetid: E0775AB3-814F-4420-9764-333572DAD201
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IUIAutomation5 interface [Windows Accessibility],RemoveNotificationEventHandler method, IUIAutomation5.RemoveNotificationEventHandler, IUIAutomation5::RemoveNotificationEventHandler, RemoveNotificationEventHandler, RemoveNotificationEventHandler method [Windows Accessibility], RemoveNotificationEventHandler method [Windows Accessibility],IUIAutomation5 interface, uiautomationclient/IUIAutomation5::RemoveNotificationEventHandler, winauto.uiauto_IUIAutomation5_RemoveNotificationEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAutomation5.RemoveNotificationEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation5::RemoveNotificationEventHandler


## -description


Removes a notification event handler.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/7E12B8C2-D6A7-4637-9049-312B78EC01DE">IUIAutomationNotificationEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="https://msdn.microsoft.com/1E6A4683-9439-4212-9EA6-91719A515C4B">AddNotificationEventHandler</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BCF67DB0-DF5B-4CED-9C32-01F126494129">IUIAutomation5</a>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>
 

 

