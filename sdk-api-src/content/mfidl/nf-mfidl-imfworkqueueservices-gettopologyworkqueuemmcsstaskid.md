---
UID: NF:mfidl.IMFWorkQueueServices.GetTopologyWorkQueueMMCSSTaskId
title: IMFWorkQueueServices::GetTopologyWorkQueueMMCSSTaskId (mfidl.h)
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified branch of the current topology.
old-location: mf\imfworkqueueservices_gettopologyworkqueuemmcsstaskid.htm
tech.root: medfound
ms.assetid: 0d519b96-428f-4cad-affc-2e94cdf28ae7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0d519b96-428f-4cad-affc-2e94cdf28ae7, GetTopologyWorkQueueMMCSSTaskId, GetTopologyWorkQueueMMCSSTaskId method [Media Foundation], GetTopologyWorkQueueMMCSSTaskId method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],GetTopologyWorkQueueMMCSSTaskId method, IMFWorkQueueServices.GetTopologyWorkQueueMMCSSTaskId, IMFWorkQueueServices::GetTopologyWorkQueueMMCSSTaskId, mf.imfworkqueueservices_gettopologyworkqueuemmcsstaskid, mfidl/IMFWorkQueueServices::GetTopologyWorkQueueMMCSSTaskId
ms.topic: method
f1_keywords: 
 - "mfidl/IMFWorkQueueServices.GetTopologyWorkQueueMMCSSTaskId"
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
 - IMFWorkQueueServices.GetTopologyWorkQueueMMCSSTaskId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFWorkQueueServices::GetTopologyWorkQueueMMCSSTaskId


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified branch of the current topology.




## -parameters




### -param dwTopologyWorkQueueId [in]

Identifies the work queue assigned to this topology branch. The application defines this value by setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-toponode-workqueue-id-attribute">MF_TOPONODE_WORKQUEUE_ID</a> attribute on the source node for the branch.


### -param pdwTaskId [out]

Receives the task identifier.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>
 

 

