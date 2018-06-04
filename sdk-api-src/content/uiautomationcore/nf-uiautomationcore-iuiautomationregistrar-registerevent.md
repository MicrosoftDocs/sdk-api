---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAutomationRegistrar::RegisterEvent


## -description


Registers a third-party Microsoft UI Automation event.


## -parameters




### -param event [in]

Type: <b><a href="https://msdn.microsoft.com/05dd033f-3bb2-4185-9cfc-c19927a82406">UIAutomationEventInfo</a>*</b>

A pointer to a  structure that contains information about the event to register.


### -param eventId [out]

Type: <b>EVENTID*</b>

Receives the event identifier. For a list of event IDs, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event ID can be used in various event methods, and as a WinEvent value for events in <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> implementations.




## -see-also




<a href="https://msdn.microsoft.com/b5d979aa-7a87-4d6c-acdc-6e9eb19aac98">IUIAutomationRegistrar</a>
 

 

