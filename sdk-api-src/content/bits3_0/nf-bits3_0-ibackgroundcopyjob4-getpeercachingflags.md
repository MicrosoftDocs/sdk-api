---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBackgroundCopyJob4::GetPeerCachingFlags


## -description


Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.


## -parameters




### -param pFlags [out]

Flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers. The following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_JOB_ENABLE_PEERCACHING_CLIENT"></a><a id="bg_job_enable_peercaching_client"></a><dl>
<dt><b>BG_JOB_ENABLE_PEERCACHING_CLIENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The job can download content from peers.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_JOB_ENABLE_PEERCACHING_SERVER"></a><a id="bg_job_enable_peercaching_server"></a><dl>
<dt><b>BG_JOB_ENABLE_PEERCACHING_SERVER</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The files of the job can be cached and served to peers.

</td>
</tr>
</table>
 


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
If other flag values are set.

</td>
</tr>
</table>
 




## -remarks



BITS can download from peers only if peercaching is enabled both at the computer level and at the job level; this API affects only the job level. For details, see <a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a>.




## -see-also




<a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">Group Policies</a>



<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>



<a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a>



<a href="https://msdn.microsoft.com/caa54ee0-c771-47e7-95d1-26a812f0f95f">IBitsPeerCacheAdministration::GetConfigurationFlags</a>



<a href="https://msdn.microsoft.com/1ede7c58-bc6d-4930-bca6-e4f26f97c648">IBitsPeerCacheAdministration::SetConfigurationFlags</a>
 

 

