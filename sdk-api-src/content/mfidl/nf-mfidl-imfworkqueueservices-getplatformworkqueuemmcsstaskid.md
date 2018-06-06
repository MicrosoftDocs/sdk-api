---
UID: NF:mfidl.IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId
title: IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified platform work queue.
old-location: mf\imfworkqueueservices_getplatformworkqueuemmcsstaskid.htm
old-project: medfound
ms.assetid: 897a048a-44fc-4176-acd9-5944f184b34a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 897a048a-44fc-4176-acd9-5944f184b34a, GetPlatformWorkQueueMMCSSTaskId, GetPlatformWorkQueueMMCSSTaskId method [Media Foundation], GetPlatformWorkQueueMMCSSTaskId method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],GetPlatformWorkQueueMMCSSTaskId method, IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId, IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId, mf.imfworkqueueservices_getplatformworkqueuemmcsstaskid, mfidl/IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified platform work queue.




## -parameters




### -param dwPlatformWorkQueueId [in]

Platform work queue to query. See <a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a>.


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




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

