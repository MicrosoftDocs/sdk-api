---
UID: NF:relogger.ITraceEvent.SetProcessId
title: ITraceEvent::SetProcessId
author: windows-sdk-content
description: Assigns an event to a specific process.
old-location: etw\ievent_setprocessid.htm
tech.root: etw
ms.assetid: c2e5e6bf-cdff-42fa-9352-2f234f39849d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITraceEvent interface [ETW],SetProcessId method, ITraceEvent.SetProcessId, ITraceEvent::SetProcessId, SetProcessId, SetProcessId method [ETW], SetProcessId method [ETW],ITraceEvent interface, etw.ievent_setprocessid, relogger/ITraceEvent::SetProcessId
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
 - ITraceEvent.SetProcessId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEvent::SetProcessId


## -description


The <b>SetProcessId</b> method assigns an event to a specific process.


## -parameters




### -param ProcessId [in]

Type: <b>ULONG</b>

Identifier of the process that should own this event.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>
 

 

