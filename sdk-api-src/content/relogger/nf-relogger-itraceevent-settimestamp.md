---
UID: NF:relogger.ITraceEvent.SetTimeStamp
title: ITraceEvent::SetTimeStamp
author: windows-sdk-content
description: Sets the time at which an event occurred.
old-location: etw\ievent_settimestamp.htm
tech.root: etw
ms.assetid: e1f76887-8edd-414e-bee3-36b61709c2b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITraceEvent interface [ETW],SetTimeStamp method, ITraceEvent.SetTimeStamp, ITraceEvent::SetTimeStamp, SetTimeStamp, SetTimeStamp method [ETW], SetTimeStamp method [ETW],ITraceEvent interface, etw.ievent_settimestamp, relogger/ITraceEvent::SetTimeStamp
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
 - ITraceEvent.SetTimeStamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEvent::SetTimeStamp


## -description


The <b>SetTimeStamp</b> method sets the time at which an event occurred.


## -parameters




### -param TimeStamp [in]

Type: <b>LARGE_INTEGER*</b>

 The time at which the event occurred, in system time.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>
 

 

