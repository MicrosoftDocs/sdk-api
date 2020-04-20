---
UID: NF:uiautomationcore.IUIAutomationRegistrar.RegisterEvent
title: IUIAutomationRegistrar::RegisterEvent (uiautomationcore.h)
description: Registers a third-party Microsoft UI Automation event.helpviewer_keywords: ["IUIAutomationRegistrar interface [Windows Accessibility]","RegisterEvent method","IUIAutomationRegistrar.RegisterEvent","IUIAutomationRegistrar::RegisterEvent","RegisterEvent","RegisterEvent method [Windows Accessibility]","RegisterEvent method [Windows Accessibility]","IUIAutomationRegistrar interface","uiauto.uiauto_IUIAutomationRegistrar_RegisterEvent","uiauto_IUIAutomationRegistrar_RegisterEvent","uiautomationcore/IUIAutomationRegistrar::RegisterEvent","winauto.uiauto_IUIAutomationRegistrar_RegisterEvent"]
old-location: winauto\uiauto_IUIAutomationRegistrar_RegisterEvent.htm
tech.root: WinAuto
ms.assetid: 17a95b6c-5dfb-45b3-92a9-0291b7d7120f
ms.date: 12/05/2018
ms.keywords: IUIAutomationRegistrar interface [Windows Accessibility],RegisterEvent method, IUIAutomationRegistrar.RegisterEvent, IUIAutomationRegistrar::RegisterEvent, RegisterEvent, RegisterEvent method [Windows Accessibility], RegisterEvent method [Windows Accessibility],IUIAutomationRegistrar interface, uiauto.uiauto_IUIAutomationRegistrar_RegisterEvent, uiauto_IUIAutomationRegistrar_RegisterEvent, uiautomationcore/IUIAutomationRegistrar::RegisterEvent, winauto.uiauto_IUIAutomationRegistrar_RegisterEvent
f1_keywords:
- uiautomationcore/IUIAutomationRegistrar.RegisterEvent
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
- UIAutomationCore.h
api_name:
- IUIAutomationRegistrar.RegisterEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationRegistrar::RegisterEvent


## -description


Registers a third-party Microsoft UI Automation event.


## -parameters




### -param event [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationeventinfo">UIAutomationEventInfo</a>*</b>

A pointer to a  structure that contains information about the event to register.


### -param eventId [out]

Type: <b>EVENTID*</b>

Receives the event identifier. For a list of event IDs, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event ID can be used in various event methods, and as a WinEvent value for events in <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> implementations.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationregistrar">IUIAutomationRegistrar</a>
 

 

