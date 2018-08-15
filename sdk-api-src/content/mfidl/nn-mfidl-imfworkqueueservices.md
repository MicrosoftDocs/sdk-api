---
UID: NN:mfidl.IMFWorkQueueServices
title: IMFWorkQueueServices
author: windows-sdk-content
description: Controls the work queues created by the Media Session.
old-location: mf\imfworkqueueservices.htm
old-project: medfound
ms.assetid: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d, IMFWorkQueueServices, IMFWorkQueueServices interface [Media Foundation], IMFWorkQueueServices interface [Media Foundation],described, mf.imfworkqueueservices, mfidl/IMFWorkQueueServices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices interface


## -description


Controls the work queues created by the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>.

The Media Session exposes this interface as a service. To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the Media Session with the service identifier MF_WORKQUEUE_SERVICES.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFWorkQueueServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFWorkQueueServices</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">BeginRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62256ae8-a18a-4160-9f3f-a08ab3e93d6b">BeginRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Registers the topology work queues with the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e15c6ff9-b72e-4e5d-a738-6bef08782e1b">BeginUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Unregisters a platform work queue from an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af68b792-6e00-4ed1-91f8-f275288dc680">BeginUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Unregisters the topology work queues from the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5">EndRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to associate a platform work queue with an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42eb1a1c-3287-4dee-ab95-fd047a16e345">EndRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to register the topology work queues with the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6cce9d8-7f6c-4835-96a4-a2e836c61d08">EndUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to unregister a platform work queue from an MMCSS task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b767e34-172c-4845-91f9-0af92a3347ab">EndUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to unregister the topology work queues from the MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f953a54b-2bc0-4ddc-9837-57f72e564c02">GetPlaftormWorkQueueMMCSSClass</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS class for a specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/897a048a-44fc-4176-acd9-5944f184b34a">GetPlatformWorkQueueMMCSSTaskId</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS task identifier for a specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e815bde7-e17e-4616-8a3f-688f357e8009">GetTopologyWorkQueueMMCSSClass</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS class for a specified branch of the current topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d519b96-428f-4cad-affc-2e94cdf28ae7">GetTopologyWorkQueueMMCSSTaskId</a>
</td>
<td align="left" width="63%">
Retrieves the MMCSS task identifier for a specified branch of the current topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/158497a9-9d66-4e58-919d-e35765fd29e4">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">BeginRegisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea258c9-1f7f-4324-a17a-d044a4864ea4">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/62256ae8-a18a-4160-9f3f-a08ab3e93d6b">BeginRegisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3117086-268e-4e52-acfb-2c8167adaa07">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/e15c6ff9-b72e-4e5d-a738-6bef08782e1b">BeginUnregisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a168462-400d-46c9-a489-7b861770469f">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/af68b792-6e00-4ed1-91f8-f275288dc680">BeginUnregisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb15129e-a3ad-4351-a7d6-dd4b883437bd">RemoteEndRegisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5">EndRegisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94dce412-6a72-4ddf-86a3-5176ee1eb6d2">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/42eb1a1c-3287-4dee-ab95-fd047a16e345">EndRegisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92eef511-0af0-4146-ac81-7dfa4a649016">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/e6cce9d8-7f6c-4835-96a4-a2e836c61d08">EndUnregisterPlatformWorkQueueWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8767a145-07b9-4427-9446-cee25e9074fa">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/6b767e34-172c-4845-91f9-0af92a3347ab">EndUnregisterTopologyWorkQueuesWithMMCSS</a>. (Not used by applications.)

</td>
</tr>
</table> 


## -remarks



If the application is using the protected media path (PMP) session, the methods in this interface automatically marshal the calls to the PMP process.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

