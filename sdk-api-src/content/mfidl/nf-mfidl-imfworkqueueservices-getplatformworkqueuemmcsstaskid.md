---
UID: NF:mfidl.IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId
title: IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId (mfidl.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified platform work queue.
helpviewer_keywords: ["897a048a-44fc-4176-acd9-5944f184b34a","GetPlatformWorkQueueMMCSSTaskId","GetPlatformWorkQueueMMCSSTaskId method [Media Foundation]","GetPlatformWorkQueueMMCSSTaskId method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","GetPlatformWorkQueueMMCSSTaskId method","IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId","IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId","mf.imfworkqueueservices_getplatformworkqueuemmcsstaskid","mfidl/IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId"]
old-location: mf\imfworkqueueservices_getplatformworkqueuemmcsstaskid.htm
tech.root: mf
ms.assetid: 897a048a-44fc-4176-acd9-5944f184b34a
ms.date: 12/05/2018
ms.keywords: 897a048a-44fc-4176-acd9-5944f184b34a, GetPlatformWorkQueueMMCSSTaskId, GetPlatformWorkQueueMMCSSTaskId method [Media Foundation], GetPlatformWorkQueueMMCSSTaskId method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],GetPlatformWorkQueueMMCSSTaskId method, IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId, IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId, mf.imfworkqueueservices_getplatformworkqueuemmcsstaskid, mfidl/IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId
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
 - IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId
 - mfidl/IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId
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
 - IMFWorkQueueServices.GetPlatformWorkQueueMMCSSTaskId
---

# IMFWorkQueueServices::GetPlatformWorkQueueMMCSSTaskId


## -description

Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier for a specified platform work queue.

## -parameters

### -param dwPlatformWorkQueueId [in]

Platform work queue to query. See <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a>.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>