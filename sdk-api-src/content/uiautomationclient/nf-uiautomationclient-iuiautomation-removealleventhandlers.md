---
UID: NF:uiautomationclient.IUIAutomation.RemoveAllEventHandlers
title: IUIAutomation::RemoveAllEventHandlers (uiautomationclient.h)
description: Removes all registered Microsoft UI Automation event handlers.helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","RemoveAllEventHandlers method","IUIAutomation.RemoveAllEventHandlers","IUIAutomation::RemoveAllEventHandlers","RemoveAllEventHandlers","RemoveAllEventHandlers method [Windows Accessibility]","RemoveAllEventHandlers method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_RemoveAllEventHandlers","uiauto_IUIAutomation_RemoveAllEventHandlers","uiautomationclient/IUIAutomation::RemoveAllEventHandlers","winauto.uiauto_IUIAutomation_RemoveAllEventHandlers"]
old-location: winauto\uiauto_IUIAutomation_RemoveAllEventHandlers.htm
tech.root: WinAuto
ms.assetid: 3bf6d15a-2aaf-4f94-a852-f9cbd25cd496
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RemoveAllEventHandlers method, IUIAutomation.RemoveAllEventHandlers, IUIAutomation::RemoveAllEventHandlers, RemoveAllEventHandlers, RemoveAllEventHandlers method [Windows Accessibility], RemoveAllEventHandlers method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_RemoveAllEventHandlers, uiauto_IUIAutomation_RemoveAllEventHandlers, uiautomationclient/IUIAutomation::RemoveAllEventHandlers, winauto.uiauto_IUIAutomation_RemoveAllEventHandlers
f1_keywords:
- uiautomationclient/IUIAutomation.RemoveAllEventHandlers
dev_langs:
- c++
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
- IUIAutomation.RemoveAllEventHandlers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::RemoveAllEventHandlers


## -description


Removes all registered Microsoft UI Automation event handlers.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, 
if the event is received simultaneously with the request to unsubscribe the event. The best practice 
is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count 
has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an 
access violation if an event is delivered late.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler">RemoveAutomationEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler">RemoveFocusChangedEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler">RemovePropertyChangedEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveStructureChangedEventHandler</a>
 

 

