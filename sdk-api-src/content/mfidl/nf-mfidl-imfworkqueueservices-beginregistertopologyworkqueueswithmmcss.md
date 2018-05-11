---
UID: NF:mfidl.IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS
author: windows-driver-content
description: Registers the topology work queues with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfworkqueueservices_beginregistertopologyworkqueueswithmmcss.htm
old-project: medfound
ms.assetid: 62256ae8-a18a-4160-9f3f-a08ab3e93d6b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 62256ae8-a18a-4160-9f3f-a08ab3e93d6b, BeginRegisterTopologyWorkQueuesWithMMCSS, BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation], BeginRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginRegisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_beginregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFWorkQueueServices.BeginRegisterTopologyWorkQueuesWithMMCSS
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS


## -description



Registers the topology work queues with the Multimedia Class Scheduler Service (MMCSS).




## -parameters




### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each source node in the topology defines one branch of the topology. The branch includes every topology node that receives data from that node. An application can assign each branch of a topology its own work queue and then associate those work queues with MMCSS tasks. 

To use this method, perform the following steps.

<ol>
<li>Create the topology.</li>
<li>Set the following attributes on the source nodes in the topology.<ul>
<li>
<a href="https://msdn.microsoft.com/5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8">MF_TOPONODE_WORKQUEUE_ID</a>. Specifies an identifier for the work queue.
          The Media Session will allocate a new work queue.</li>
<li>
<a href="https://msdn.microsoft.com/8668d0f1-9d54-4c56-bb19-09498252bec4">MF_TOPONODE_WORKQUEUE_MMCSS_CLASS</a>. Specifies the MMCSS class.
          </li>
<li>
<a href="https://msdn.microsoft.com/ccecc1e6-2d30-4e89-849f-c3acad97f312">MF_TOPONODE_WORKQUEUE_MMCSS_TASKID</a>. Specifies the MMCSS task identifier (optional). If this attribute is not set, MMCSS assigns a new task identifier.
          </li>
</ul>
</li>
<li>Queue the topology by calling <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a>.</li>
<li>Wait for the <a href="https://msdn.microsoft.com/b45fd598-ab1e-4b12-8d82-c88c96d1f770">MESessionTopologyStatus</a> event with the <b>MF_TOPOSTATUS_READY</b>  status.</li>
<li>Call <b>BeginRegisterTopologyWorkQueuesWithMMCSS</b>. This method registers all of the topology work queues with MMCSS.</li>
</ol>
The <b>BeginRegisterTopologyWorkQueuesWithMMCSS</b> method is asynchronous. When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. Within the callback method, call <a href="https://msdn.microsoft.com/42eb1a1c-3287-4dee-ab95-fd047a16e345">IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS</a> to complete the asynchronous request. After this operation completes, the Media Session automatically registers the work queues for every new topology that is queued on the Media Session. The application does not need to call the method again for new topologies.

To unregister the topology work queues from MMCSS, call <a href="https://msdn.microsoft.com/af68b792-6e00-4ed1-91f8-f275288dc680">IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

