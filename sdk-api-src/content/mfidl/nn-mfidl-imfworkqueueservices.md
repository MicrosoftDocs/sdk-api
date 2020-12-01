---
UID: NN:mfidl.IMFWorkQueueServices
title: IMFWorkQueueServices (mfidl.h)
description: Controls the work queues created by the Media Session.
helpviewer_keywords: ["7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d","IMFWorkQueueServices","IMFWorkQueueServices interface [Media Foundation]","IMFWorkQueueServices interface [Media Foundation]","described","mf.imfworkqueueservices","mfidl/IMFWorkQueueServices"]
old-location: mf\imfworkqueueservices.htm
tech.root: mf
ms.assetid: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d
ms.date: 12/05/2018
ms.keywords: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d, IMFWorkQueueServices, IMFWorkQueueServices interface [Media Foundation], IMFWorkQueueServices interface [Media Foundation],described, mf.imfworkqueueservices, mfidl/IMFWorkQueueServices
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
 - IMFWorkQueueServices
 - mfidl/IMFWorkQueueServices
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
 - IMFWorkQueueServices
---

# IMFWorkQueueServices interface


## -description

Controls the work queues created by the <a href="/windows/desktop/medfound/media-session">Media Session</a>.

The Media Session exposes this interface as a service. To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the Media Session with the service identifier MF_WORKQUEUE_SERVICES.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFWorkQueueServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFWorkQueueServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFWorkQueueServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss">BeginRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss">BeginRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Registers the topology work queues with the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss">BeginUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Unregisters a platform work queue from an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss">BeginUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Unregisters the topology work queues from the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss">EndRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to associate a platform work queue with an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss">EndRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to register the topology work queues with the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss">EndUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to unregister a platform work queue from an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss">EndUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to unregister the topology work queues from the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-getplaftormworkqueuemmcssclass">GetPlaftormWorkQueueMMCSSClass</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS class for a specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-getplatformworkqueuemmcsstaskid">GetPlatformWorkQueueMMCSSTaskId</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS task identifier for a specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-gettopologyworkqueuemmcssclass">GetTopologyWorkQueueMMCSSClass</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS class for a specified branch of the current topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-gettopologyworkqueuemmcsstaskid">GetTopologyWorkQueueMMCSSTaskId</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS task identifier for a specified branch of the current topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remotebeginregisterplatformworkqueuewithmmcss">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss">BeginRegisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remotebeginregistertopologyworkqueueswithmmcss">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss">BeginRegisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remotebeginunregisterplatformworkqueuewithmmcss">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss">BeginUnregisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remotebeginunregistertopologyworkqueueswithmmcss">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss">BeginUnregisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remoteendregisterplatformworkqueuewithmmcss">RemoteEndRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss">EndRegisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remoteendregistertopologyworkqueueswithmmcss">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss">EndRegisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remoteendunregisterplatformworkqueuewithmmcss">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss">EndUnregisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/medfound/imfworkqueueservices-remoteendunregistertopologyworkqueueswithmmcss">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss">EndUnregisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
</table>

## -remarks

If the application is using the protected media path (PMP) session, the methods in this interface automatically marshal the calls to the PMP process.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>