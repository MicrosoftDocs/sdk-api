---
UID: NF:mfidl.IMFRealTimeClient.SetWorkQueue
title: IMFRealTimeClient::SetWorkQueue (mfidl.h)
description: Specifies the work queue for the topology branch that contains this object.
helpviewer_keywords: ["2744ddaf-a1ad-415a-b387-1a3d3b4821bf","IMFRealTimeClient interface [Media Foundation]","SetWorkQueue method","IMFRealTimeClient.SetWorkQueue","IMFRealTimeClient::SetWorkQueue","SetWorkQueue","SetWorkQueue method [Media Foundation]","SetWorkQueue method [Media Foundation]","IMFRealTimeClient interface","mf.imfrealtimeclient_setworkqueue","mfidl/IMFRealTimeClient::SetWorkQueue"]
old-location: mf\imfrealtimeclient_setworkqueue.htm
tech.root: mf
ms.assetid: 2744ddaf-a1ad-415a-b387-1a3d3b4821bf
ms.date: 12/05/2018
ms.keywords: 2744ddaf-a1ad-415a-b387-1a3d3b4821bf, IMFRealTimeClient interface [Media Foundation],SetWorkQueue method, IMFRealTimeClient.SetWorkQueue, IMFRealTimeClient::SetWorkQueue, SetWorkQueue, SetWorkQueue method [Media Foundation], SetWorkQueue method [Media Foundation],IMFRealTimeClient interface, mf.imfrealtimeclient_setworkqueue, mfidl/IMFRealTimeClient::SetWorkQueue
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRealTimeClient::SetWorkQueue
 - mfidl/IMFRealTimeClient::SetWorkQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRealTimeClient.SetWorkQueue
---

# IMFRealTimeClient::SetWorkQueue


## -description

Specifies the work queue for the topology branch that contains this object.

## -parameters

### -param dwWorkQueueId [in]

The identifier of the work queue, or the value <b>MFASYNC_CALLBACK_QUEUE_UNDEFINED</b>. See Remarks.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application can register a branch of the topology to use a private work queue. The Media Session notifies any pipeline object that supports <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient">IMFRealTimeClient</a> by calling <b>SetWorkQueue</b> with the application's work queue identifier.
      

When the application unregisters the topology branch, the Media Session calls <b>SetWorkQueue</b> again with the value <b>MFASYNC_CALLBACK_QUEUE_UNDEFINED</b>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient">IMFRealTimeClient</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a>