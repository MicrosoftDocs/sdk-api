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
 

 

