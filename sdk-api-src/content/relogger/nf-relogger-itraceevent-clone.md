---
UID: NF:relogger.ITraceEvent.Clone
title: ITraceEvent::Clone
author: windows-sdk-content
description: Creates a duplicate copy of an event.
old-location: etw\ievent_clone.htm
tech.root: etw
ms.assetid: a4fa29f4-a265-4b42-a499-bc53566dc889
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [ETW], Clone method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],Clone method, ITraceEvent.Clone, ITraceEvent::Clone, etw.ievent_clone, relogger/ITraceEvent::Clone
ms.topic: method
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
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
 - Relogger.h
api_name:
 - ITraceEvent.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEvent::Clone


## -description


The <b>Clone</b> method creates a duplicate copy of an event.


## -parameters




### -param NewEvent [out, retval]

Type: <b>IEvent**</b>

The new event.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>
 

 

