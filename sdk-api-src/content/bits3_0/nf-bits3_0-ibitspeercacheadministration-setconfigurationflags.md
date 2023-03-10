---
UID: NF:bits3_0.IBitsPeerCacheAdministration.SetConfigurationFlags
title: IBitsPeerCacheAdministration::SetConfigurationFlags (bits3_0.h)
description: Sets the configuration flags that determine if the computer can serve content to peers and can download content from peers.
helpviewer_keywords: ["BG_ENABLE_PEERCACHING_CLIENT","BG_ENABLE_PEERCACHING_SERVER","IBitsPeerCacheAdministration interface [BITS]","SetConfigurationFlags method","IBitsPeerCacheAdministration.SetConfigurationFlags","IBitsPeerCacheAdministration::SetConfigurationFlags","SetConfigurationFlags","SetConfigurationFlags method [BITS]","SetConfigurationFlags method [BITS]","IBitsPeerCacheAdministration interface","bits.ibitspeercacheadministration_setconfigurationflags","bits3_0/IBitsPeerCacheAdministration::SetConfigurationFlags"]
old-location: bits\ibitspeercacheadministration_setconfigurationflags.htm
tech.root: Bits
ms.assetid: 1ede7c58-bc6d-4930-bca6-e4f26f97c648
ms.date: 12/05/2018
ms.keywords: BG_ENABLE_PEERCACHING_CLIENT, BG_ENABLE_PEERCACHING_SERVER, IBitsPeerCacheAdministration interface [BITS],SetConfigurationFlags method, IBitsPeerCacheAdministration.SetConfigurationFlags, IBitsPeerCacheAdministration::SetConfigurationFlags, SetConfigurationFlags, SetConfigurationFlags method [BITS], SetConfigurationFlags method [BITS],IBitsPeerCacheAdministration interface, bits.ibitspeercacheadministration_setconfigurationflags, bits3_0/IBitsPeerCacheAdministration::SetConfigurationFlags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitsPeerCacheAdministration::SetConfigurationFlags
 - bits3_0/IBitsPeerCacheAdministration::SetConfigurationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.SetConfigurationFlags
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

BITS will not download files from a peer unless both the client computer and the job permit BITS to download files from a peer. To permits the job to download files from a peer, call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a> method and set the BG_JOB_ENABLE_PEERCACHING_CLIENT flag.

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

BITS will not cache the files and serve them to peers unless both the client computer and job permit BITS to cache and serve files. To permit the job to cache files for a job, call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a> method and set the BG_JOB_ENABLE_PEERCACHING_SERVER flag.

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

A job determines if it downloads content from a peer or serves its content to peers. For details, see the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a> method.

## -see-also

<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags">IBitsPeerCacheAdministration::GetConfigurationFlags</a>