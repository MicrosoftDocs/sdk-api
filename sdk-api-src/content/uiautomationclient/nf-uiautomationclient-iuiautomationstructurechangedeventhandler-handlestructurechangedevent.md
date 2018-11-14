---
UID: NF:uiautomationclient.IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent
title: IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent
author: windows-sdk-content
description: Handles an event that is raised when the Microsoft UI Automation tree structure has changed.
old-location: winauto\uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent.htm
tech.root: WinAuto
ms.assetid: 0fdaf2d3-cfd1-4c93-a7cd-94ec83b3e812
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HandleStructureChangedEvent, HandleStructureChangedEvent method [Windows Accessibility], HandleStructureChangedEvent method [Windows Accessibility],IUIAutomationStructureChangedEventHandler interface, IUIAutomationStructureChangedEventHandler interface [Windows Accessibility],HandleStructureChangedEvent method, IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent, IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent, uiauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent, uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent, uiautomationclient/IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent, winauto.uiauto_IUIAutomationStructureChangedEventHandler_HandleStructureChangedEvent
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
 - IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomationStructureChangedEventHandler.HandleStructureChangedEvent
: 
---

# IUIAutomationStructureChangedEventHandler::HandleStructureChangedEvent


## -description


Handles an event that is raised when the Microsoft UI Automation tree structure has changed.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element that raised the event.


### -param arg2 [in]

Type: <b><a href="https://msdn.microsoft.com/abaf9551-40c4-4ab6-adb7-b619f3bc9745">StructureChangeType</a></b>

A value indicating the type of tree structure change that took place.


### -param runtimeId [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

Receives the runtime identifier of the element. This parameter is used only when <i>changeType</i> is <a href="uiauto_StructureChangeTypeEnum.htm">StructureChangeType_ChildRemoved</a>; it is <b>NULL</b> for all other structure-change events. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/671049a4-50cf-49df-9028-7af38629b7a9">AddStructureChangedEventHandler</a>


Adjusting an event handler from within this method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/a28ad163-d931-432a-a786-646a10baaf86">IUIAutomationStructureChangedEventHandler</a>
 

 

