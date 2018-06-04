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

# CoHandlePriorityEventsFromMessagePump function


## -description


Called by message dispatchers on an ASTA thread after dispatching a windows message to provide an opportunity for short-running infrastructural COM calls and other high-priority or short-running COM work to be dispatched between messages. This helps to provide similar responsiveness to these infrastructural calls in an ASTA as in a classic STA, even when there is a long stream of window messages to be handled.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function dispatches any high-priority COM calls or work that are queued on the ASTA thread, then returns. It returns quickly if there is no work to perform.

This function silently does nothing when called on non-ASTA threads.




