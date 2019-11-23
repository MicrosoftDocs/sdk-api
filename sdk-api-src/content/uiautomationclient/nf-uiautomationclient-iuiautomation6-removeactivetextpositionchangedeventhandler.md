---
UID: NF:uiautomationclient.IUIAutomation6.RemoveActiveTextPositionChangedEventHandler
title: IUIAutomation6::RemoveActiveTextPositionChangedEventHandler (uiautomationclient.h)

description: Removes an active text position changed event handler.
old-location: winauto\uiauto_IUIAutomation6_RemoveActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 92A6E9BA-0B68-4890-90EE-16F4B0929340

ms.date: 12/05/2018
ms.keywords: IUIAutomation6 interface [Windows Accessibility],RemoveActiveTextPositionChangedEventHandler method, IUIAutomation6.RemoveActiveTextPositionChangedEventHandler, IUIAutomation6::RemoveActiveTextPositionChangedEventHandler, RemoveActiveTextPositionChangedEventHandler, RemoveActiveTextPositionChangedEventHandler method [Windows Accessibility], RemoveActiveTextPositionChangedEventHandler method [Windows Accessibility],IUIAutomation6 interface, uiautomationclient/IUIAutomation6::RemoveActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomation6_RemoveActiveTextPositionChangedEventHandler
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomation6.RemoveActiveTextPositionChangedEventHandler"
dev_langs:
 - c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
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
 - IUIAutomation6.RemoveActiveTextPositionChangedEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# IUIAutomation6::RemoveActiveTextPositionChangedEventHandler


## -description


Removes an active text position changed event handler.


## -parameters




### -param element [in]

A pointer to the UI Automation element associated with the event handler.


### -param handler [in]

A pointer to the object that handles the active text position changed event.



## -returns



This method does not return a value.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, if the event is received simultaneously with the request to unsubscribe the event. The best practice is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an access violation if an event is delivered late.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-addactivetextpositionchangedeventhandler">AddActiveTextPositionChangedEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6">IUIAutomation6</a>
 

 

