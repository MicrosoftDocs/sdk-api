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

# IWbemEventSink::SetBatchingParameters


## -description


The 
<b>IWbemEventSink::SetBatchingParameters</b> method is used to set the maximum event buffer size and its associated processing latency value.


## -parameters




### -param lFlags [in]

Determines batching behavior.



#### WBEM_FLAG_BATCH_IF_NEEDED (0)

System determines if batching is used.



#### WBEM_FLAG_MUST_BATCH (0x1)

Batching required.



#### WBEM_FLAG_MUST_NOT_BATCH (0x2)

Do not batch.


### -param dwMaxBufferSize [in]

Maximum batch buffer size. To specify maximum batch size, use MAX_INT.


### -param dwMaxSendLatency [in]

Maximum batch send latency. To specify infinite timeout, use <b>WBEM_INFINITE</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.



