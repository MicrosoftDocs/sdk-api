---
UID: NF:relogger.ITraceEvent.GetUserContext
title: ITraceEvent::GetUserContext
author: windows-sdk-content
description: Retrieves the user context associated with the stream to which the event belongs.
old-location: etw\ievent_getusercontext.htm
old-project: ETW
ms.assetid: 9d4d8abd-b48a-487b-bb73-a6fa48c512c7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetUserContext, GetUserContext method [ETW], GetUserContext method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],GetUserContext method, ITraceEvent.GetUserContext, ITraceEvent::GetUserContext, etw.ievent_getusercontext, relogger/ITraceEvent::GetUserContext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RECO_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceEvent.GetUserContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITraceEvent::GetUserContext


## -description


The <b>GetUserContext</b> method retrieves the user context associated with the stream to which the event belongs.


## -parameters




### -param UserContext [out, retval]

Type: <b>void**</b>

The user context. This is the context specified in the call to <a href="https://msdn.microsoft.com/2bdf6175-f4c6-4217-a37a-b2af32ad38c6">ITraceRelogger::AddLogfileTraceStream</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>



<a href="https://msdn.microsoft.com/2bdf6175-f4c6-4217-a37a-b2af32ad38c6">ITraceRelogger::AddLogfileTraceStream</a>



<a href="https://msdn.microsoft.com/68bb5715-49b8-45bc-ae98-0b4a519c8e62">ITraceRelogger::AddRealtimeTraceStream</a>
 

 

