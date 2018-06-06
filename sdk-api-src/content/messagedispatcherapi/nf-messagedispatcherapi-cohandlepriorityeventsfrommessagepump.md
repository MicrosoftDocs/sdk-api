---
UID: NF:messagedispatcherapi.CoHandlePriorityEventsFromMessagePump
title: CoHandlePriorityEventsFromMessagePump function
author: windows-sdk-content
description: Called by message dispatchers on an ASTA thread after dispatching a windows message to provide an opportunity for short-running infrastructural COM calls and other high-priority or short-running COM work to be dispatched between messages.
old-location: com\cohandlepriorityeventsfrommessagepump.htm
old-project: com
ms.assetid: 24EA766D-82F8-4E57-AAB8-A06ECE644319
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoHandlePriorityEventsFromMessagePump, CoHandlePriorityEventsFromMessagePump function [COM], com.cohandlepriorityeventsfrommessagepump, messagedispatcherapi/CoHandlePriorityEventsFromMessagePump
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: messagedispatcherapi.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ole32.dll
api_name:
 - CoHandlePriorityEventsFromMessagePump
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: GDI+ 1.1
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




