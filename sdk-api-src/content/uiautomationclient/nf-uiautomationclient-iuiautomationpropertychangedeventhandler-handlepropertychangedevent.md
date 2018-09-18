---
UID: NF:uiautomationclient.IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent
title: IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent
author: windows-sdk-content
description: Handles a Microsoft UI Automation property-changed event.
old-location: winauto\uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent.htm
tech.root: WinAuto
ms.assetid: 3b0bb9a0-b2a5-4843-9431-cc00e1836dd1
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: HandlePropertyChangedEvent, HandlePropertyChangedEvent method [Windows Accessibility], HandlePropertyChangedEvent method [Windows Accessibility],IUIAutomationPropertyChangedEventHandler interface, IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility],HandlePropertyChangedEvent method, IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent, IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent, uiauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent, uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent, uiautomationclient/IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent, winauto.uiauto_IUIAutomationPropertyChangedEventHandler_HandlePropertyChangedEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IUIAutomationPropertyChangedEventHandler.HandlePropertyChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent


## -description


Handles a Microsoft UI Automation property-changed event.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The identifier of the property whose value has changed. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param newValue [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The new property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>.
			

Adjusting an event handler from within this method is not supported.



