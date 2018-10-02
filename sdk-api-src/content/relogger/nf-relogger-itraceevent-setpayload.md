---
UID: NF:relogger.ITraceEvent.SetPayload
title: ITraceEvent::SetPayload
author: windows-sdk-content
description: Sets the payload for an event.
old-location: etw\ievent_setpayload.htm
tech.root: ETW
ms.assetid: 180e0487-5262-45ae-a701-3fcb575637ae
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITraceEvent interface [ETW],SetPayload method, ITraceEvent.SetPayload, ITraceEvent::SetPayload, SetPayload, SetPayload method [ETW], SetPayload method [ETW],ITraceEvent interface, etw.ievent_setpayload, relogger/ITraceEvent::SetPayload
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITraceEvent.SetPayload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEvent::SetPayload


## -description


The <b>SetPayload</b> method sets the payload for an event.


## -parameters




### -param Payload [in]

Type: <b>BYTE*</b>

The event payload data.


### -param PayloadSize [in]

Type: <b>ULONG</b>

Size of the payload data, in bytes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Payloads contain only developer-defined data.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>
 

 

