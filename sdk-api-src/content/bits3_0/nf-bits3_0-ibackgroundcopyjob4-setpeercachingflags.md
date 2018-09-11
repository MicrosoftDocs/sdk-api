---
UID: NF:bits3_0.IBackgroundCopyJob4.SetPeerCachingFlags
title: IBackgroundCopyJob4::SetPeerCachingFlags
author: windows-sdk-content
description: Sets flags that determine if the files of the job can be cached and served to peers and if the job can download content from peers.
old-location: bits\ibackgroundcopyjob4_setpeercachingflags.htm
tech.root: bits
ms.assetid: 53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_JOB_DISABLE_BRANCH_CACHE, BG_JOB_ENABLE_PEERCACHING_CLIENT, BG_JOB_ENABLE_PEERCACHING_SERVER, IBackgroundCopyJob4 interface [BITS],SetPeerCachingFlags method, IBackgroundCopyJob4.SetPeerCachingFlags, IBackgroundCopyJob4::SetPeerCachingFlags, SetPeerCachingFlags, SetPeerCachingFlags method [BITS], SetPeerCachingFlags method [BITS],IBackgroundCopyJob4 interface, bits.ibackgroundcopyjob4_setpeercachingflags, bits3_0/IBackgroundCopyJob4::SetPeerCachingFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
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
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.SetPeerCachingFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob4::SetPeerCachingFlags


## -description


Sets flags that determine if the files of the job can be cached and served to peers and if the job can download content from peers.


## -parameters




### -param Flags [in]

Flags that determine if the files of the job can be cached and served to peers and if the job can download content from peers. The following flags can be set:

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

The job will not download from a peer unless both the client computer and the job allow Background Intelligent Transfer Service (BITS) to download files from a peer. To enable the client computer to download files from a peer, set the <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">EnablePeerCaching</a> group policy or call the <a href="https://msdn.microsoft.com/en-us/library/Aa964288(v=VS.85).aspx">IBitsPeerCacheAdministration::SetConfigurationFlags</a> method and set the BG_ENABLE_PEERCACHING_CLIENT flag.

If one of the following conditions exists, BITS will stop the download and reschedule the job to begin transferring from either a peer or the origin server, depending on the value for the job and the cache:<ul>
<li>This value for the cache is <b>TRUE</b> and the value for the job toggles between <b>TRUE</b> and <b>FALSE</b>.</li>
<li>This value for the job property is <b>TRUE</b> and the value for the cache toggles between <b>TRUE</b> and <b>FALSE</b>.</li>
</ul>The download will then resume from where it left off before BITS stopped the job.<b>BITS 4.0:  </b>This flag is deprecated.



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

BITS will not cache the files and serve them to peers unless both the client computer and job allow BITS to cache and serve the files. To allow BITS to cache and serve the files on the client computer, set the <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">EnablePeerCaching</a> group policy or call the <a href="https://msdn.microsoft.com/en-us/library/Aa964288(v=VS.85).aspx">IBitsPeerCacheAdministration::SetConfigurationFlags</a> method and set the BG_ENABLE_PEERCACHING_SERVER flag.<b>BITS 4.0:  </b>This flag is deprecated.



</td>
</tr>
<tr>
<td width="40%"><a id="BG_JOB_DISABLE_BRANCH_CACHE"></a><a id="bg_job_disable_branch_cache"></a><dl>
<dt><b>BG_JOB_DISABLE_BRANCH_CACHE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
BITS will not use Windows BranchCache for transfer jobs. This setting does not affect the use of Windows BranchCache by applications other than BITS. 

</td>
</tr>
</table>
 


## -returns



The method returns the following values.

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
</table>
 




## -remarks



Setting these flags has meaning only if the peer caching has been enabled by either setting the  <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">EnablePeerCaching</a> group policy or calling the <a href="https://msdn.microsoft.com/en-us/library/Aa964288(v=VS.85).aspx">IBitsPeerCacheAdministration::SetConfigurationFlags</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362995(v=VS.85).aspx">IBackgroundCopyJob4</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964247(v=VS.85).aspx">IBackgroundCopyJob4::GetPeerCachingFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964288(v=VS.85).aspx">IBitsPeerCacheAdministration::SetConfigurationFlags</a>
 

 

