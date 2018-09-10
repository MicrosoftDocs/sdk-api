---
UID: NN:mfidl.IMFRealTimeClient
title: IMFRealTimeClient
author: windows-sdk-content
description: Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfrealtimeclient.htm
tech.root: medfound
ms.assetid: b1d1901e-dd49-421f-9212-61e32cff411e
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFRealTimeClient, IMFRealTimeClient interface [Media Foundation], IMFRealTimeClient interface [Media Foundation],described, b1d1901e-dd49-421f-9212-61e32cff411e, mf.imfrealtimeclient, mfidl/IMFRealTimeClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRealTimeClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRealTimeClient interface


## -description


Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).

Any pipeline object that creates worker threads should implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRealTimeClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRealTimeClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRealTimeClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31">RegisterThreads</a>
</td>
<td align="left" width="63%">
Notifies the object to register its worker threads with MMCSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2744ddaf-a1ad-415a-b387-1a3d3b4821bf">SetWorkQueue</a>
</td>
<td align="left" width="63%">
Specifies the work queue for the topology branch to which this object belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bd65ff1-c283-47b8-8299-383b2b773c18">UnregisterThreads</a>
</td>
<td align="left" width="63%">
Notifies the object to unregister its worker threads from MMCSS.

</td>
</tr>
</table> 


## -remarks



Media Foundation provides a mechanism for applications to associate branches in the topology with MMCSS tasks. A topology branch is defined by a source node in the topology and all of the nodes downstream from it. An application registers a topology branch with MMCSS by setting the <a href="https://msdn.microsoft.com/5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8">MF_TOPONODE_WORKQUEUE_ID</a> attribute on the source node and then calling <a href="https://msdn.microsoft.com/62256ae8-a18a-4160-9f3f-a08ab3e93d6b">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a>.

When the application registers a topology branch with MMCSS, the Media Session queries every pipeline object in that branch for the <b>IMFRealTimeClient</b> interface. If the object exposes the interface, the Media Session calls <a href="https://msdn.microsoft.com/0ed3a8f6-1ea1-44af-ac6e-8712fd59ae31">RegisterThreads</a>.

When the application unregisters the topology branch, the Media Session calls <a href="https://msdn.microsoft.com/9bd65ff1-c283-47b8-8299-383b2b773c18">UnregisterThreads</a>.

If a pipeline object creates its own worker threads but does not implement this interface, it can cause priority inversions in the Media Foundation pipeline, because high-priority processing threads might be blocked while waiting for the component to process data on a thread with lower priority.

Pipeline objects that do not create worker threads do not need to implement this interface.

In Windows 8, this interface is extended with <a href="https://msdn.microsoft.com/EC5CDD23-B862-4DAE-AC01-4926C4FAD89A">IMFRealTimeClientEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

