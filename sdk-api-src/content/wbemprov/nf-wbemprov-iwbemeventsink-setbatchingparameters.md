---
UID: NF:wbemprov.IWbemEventSink.SetBatchingParameters
title: IWbemEventSink::SetBatchingParameters (wbemprov.h)
description: The IWbemEventSink::SetBatchingParameters method is used to set the maximum event buffer size and its associated processing latency value.
helpviewer_keywords: ["IWbemEventSink interface [Windows Management Instrumentation]","SetBatchingParameters method","IWbemEventSink.SetBatchingParameters","IWbemEventSink::SetBatchingParameters","SetBatchingParameters","SetBatchingParameters method [Windows Management Instrumentation]","SetBatchingParameters method [Windows Management Instrumentation]","IWbemEventSink interface","WBEM_FLAG_BATCH_IF_NEEDED","WBEM_FLAG_MUST_BATCH","WBEM_FLAG_MUST_NOT_BATCH","_hmm_iwbemeventsink_setbatchingparameters","wbemprov/IWbemEventSink::SetBatchingParameters","wmi.iwbemeventsink_setbatchingparameters"]
old-location: wmi\iwbemeventsink_setbatchingparameters.htm
tech.root: wmi
ms.assetid: 7fcc1598-bc0c-4d4a-ad6f-69317bd789a4
ms.date: 12/05/2018
ms.keywords: IWbemEventSink interface [Windows Management Instrumentation],SetBatchingParameters method, IWbemEventSink.SetBatchingParameters, IWbemEventSink::SetBatchingParameters, SetBatchingParameters, SetBatchingParameters method [Windows Management Instrumentation], SetBatchingParameters method [Windows Management Instrumentation],IWbemEventSink interface, WBEM_FLAG_BATCH_IF_NEEDED, WBEM_FLAG_MUST_BATCH, WBEM_FLAG_MUST_NOT_BATCH, _hmm_iwbemeventsink_setbatchingparameters, wbemprov/IWbemEventSink::SetBatchingParameters, wmi.iwbemeventsink_setbatchingparameters
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemEventSink::SetBatchingParameters
 - wbemprov/IWbemEventSink::SetBatchingParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventSink.SetBatchingParameters
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

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

