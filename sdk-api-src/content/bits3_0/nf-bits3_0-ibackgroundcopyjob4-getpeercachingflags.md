---
UID: NF:bits3_0.IBackgroundCopyJob4.GetPeerCachingFlags
title: IBackgroundCopyJob4::GetPeerCachingFlags
author: windows-sdk-content
description: Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.
old-location: bits\ibackgroundcopyjob4_getpeercachingflags.htm
old-project: bits
ms.assetid: 1b9cdd81-91e8-4d24-a451-61bed51289d4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_JOB_ENABLE_PEERCACHING_CLIENT, BG_JOB_ENABLE_PEERCACHING_SERVER, GetPeerCachingFlags, GetPeerCachingFlags method [BITS], GetPeerCachingFlags method [BITS],IBackgroundCopyJob4 interface, IBackgroundCopyJob4 interface [BITS],GetPeerCachingFlags method, IBackgroundCopyJob4.GetPeerCachingFlags, IBackgroundCopyJob4::GetPeerCachingFlags, bits.ibackgroundcopyjob4_getpeercachingflags, bits3_0/IBackgroundCopyJob4::GetPeerCachingFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.GetPeerCachingFlags
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
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
 

 

