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

# IBitsPeerCacheAdministration::SetConfigurationFlags


## -description


Sets the configuration flags that determine if the computer can serve content to peers and can download content from peers.


## -parameters




### -param Flags [in]

Flags that determine if the computer can serve content to peers and can download content from peers. The following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_CLIENT"></a><a id="bg_enable_peercaching_client"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_CLIENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The computer can download content from peers.

BITS will not download files from a peer unless both the client computer and the job permit BITS to download files from a peer. To permits the job to download files from a peer, call the <a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a> method and set the BG_JOB_ENABLE_PEERCACHING_CLIENT flag.

Note that changing this value can affect all jobs on the computer. If one of the following conditions exists, BITS will stop the download and reschedule the job to begin transferring from either a peer or the origin server, depending on the value for the job and the cache:<ul>
<li>This value for the cache is <b>TRUE</b> and the value for the job toggles between <b>TRUE</b> and <b>FALSE</b>.</li>
<li>This value for the job property is <b>TRUE</b> and the value for the cache toggles between <b>TRUE</b> and <b>FALSE</b>.</li>
</ul>The download will then resume from where it left off before BITS stopped the job.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_SERVER"></a><a id="bg_enable_peercaching_server"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_SERVER</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The computer can serve content to peers.

BITS will not cache the files and serve them to peers unless both the client computer and job permit BITS to cache and serve files. To permit the job to cache files for a job, call the <a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a> method and set the BG_JOB_ENABLE_PEERCACHING_SERVER flag.

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
<dt><b>BG_S_OVERRIDDEN_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference. 

The method returns this value if the value set is different from the group policy value. If the values are the same, the method returns S_OK.

</td>
</tr>
</table>
 




## -remarks



This value is used only if the EnablePeerCaching group policy is not set.

A job determines if it downloads content from a peer or serves its content to peers. For details, see the <a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a> method.




## -see-also




<a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a>



<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/caa54ee0-c771-47e7-95d1-26a812f0f95f">IBitsPeerCacheAdministration::GetConfigurationFlags</a>
 

 

