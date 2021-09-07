---
UID: NF:mfidl.IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS (mfidl.h)
description: Registers the topology work queues with the Multimedia Class Scheduler Service (MMCSS).
helpviewer_keywords: ["62256ae8-a18a-4160-9f3f-a08ab3e93d6b","BeginRegisterTopologyWorkQueuesWithMMCSS","BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","BeginRegisterTopologyWorkQueuesWithMMCSS method","IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS","IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS","mf.imfworkqueueservices_beginregistertopologyworkqueueswithmmcss","mfidl/IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS"]
old-location: mf\imfworkqueueservices_beginregistertopologyworkqueueswithmmcss.htm
tech.root: mf
ms.assetid: 62256ae8-a18a-4160-9f3f-a08ab3e93d6b
ms.date: 12/05/2018
ms.keywords: 62256ae8-a18a-4160-9f3f-a08ab3e93d6b, BeginRegisterTopologyWorkQueuesWithMMCSS, BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation], BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginRegisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_beginregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS
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
 - IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS
 - mfidl/IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS
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
 - IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS
---

# IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS


## -description

Registers the topology work queues with the Multimedia Class Scheduler Service (MMCSS).

## -parameters

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each source node in the topology defines one branch of the topology. The branch includes every topology node that receives data from that node. An application can assign each branch of a topology its own work queue and then associate those work queues with MMCSS tasks. 

To use this method, perform the following steps.

<ol>
<li>Create the topology.</li>
<li>Set the following attributes on the source nodes in the topology.<ul>
<li>
<a href="/windows/desktop/medfound/mf-toponode-workqueue-id-attribute">MF_TOPONODE_WORKQUEUE_ID</a>. Specifies an identifier for the work queue.
          The Media Session will allocate a new work queue.</li>
<li>
<a href="/windows/desktop/medfound/mf-toponode-workqueue-mmcss-class-attribute">MF_TOPONODE_WORKQUEUE_MMCSS_CLASS</a>. Specifies the MMCSS class.
          </li>
<li>
<a href="/windows/desktop/medfound/mf-toponode-workqueue-mmcss-taskid-attribute">MF_TOPONODE_WORKQUEUE_MMCSS_TASKID</a>. Specifies the MMCSS task identifier (optional). If this attribute is not set, MMCSS assigns a new task identifier.
          </li>
</ul>
</li>
<li>Queue the topology by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a>.</li>
<li>Wait for the <a href="/windows/desktop/medfound/mesessiontopologystatus">MESessionTopologyStatus</a> event with the <b>MF_TOPOSTATUS_READY</b>  status.</li>
<li>Call <b>BeginRegisterTopologyWorkQueuesWithMMCSS</b>. This method registers all of the topology work queues with MMCSS.</li>
</ol>
The <b>BeginRegisterTopologyWorkQueuesWithMMCSS</b> method is asynchronous. When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. Within the callback method, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS</a> to complete the asynchronous request. After this operation completes, the Media Session automatically registers the work queues for every new topology that is queued on the Media Session. The application does not need to call the method again for new topologies.

To unregister the topology work queues from MMCSS, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>