---
UID: NF:bits3_0.IBackgroundCopyJob4.GetPeerCachingFlags
title: IBackgroundCopyJob4::GetPeerCachingFlags (bits3_0.h)
description: Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.
helpviewer_keywords: ["BG_JOB_ENABLE_PEERCACHING_CLIENT","BG_JOB_ENABLE_PEERCACHING_SERVER","GetPeerCachingFlags","GetPeerCachingFlags method [BITS]","GetPeerCachingFlags method [BITS]","IBackgroundCopyJob4 interface","IBackgroundCopyJob4 interface [BITS]","GetPeerCachingFlags method","IBackgroundCopyJob4.GetPeerCachingFlags","IBackgroundCopyJob4::GetPeerCachingFlags","bits.ibackgroundcopyjob4_getpeercachingflags","bits3_0/IBackgroundCopyJob4::GetPeerCachingFlags"]
old-location: bits\ibackgroundcopyjob4_getpeercachingflags.htm
tech.root: Bits
ms.assetid: 1b9cdd81-91e8-4d24-a451-61bed51289d4
ms.date: 12/05/2018
ms.keywords: BG_JOB_ENABLE_PEERCACHING_CLIENT, BG_JOB_ENABLE_PEERCACHING_SERVER, GetPeerCachingFlags, GetPeerCachingFlags method [BITS], GetPeerCachingFlags method [BITS],IBackgroundCopyJob4 interface, IBackgroundCopyJob4 interface [BITS],GetPeerCachingFlags method, IBackgroundCopyJob4.GetPeerCachingFlags, IBackgroundCopyJob4::GetPeerCachingFlags, bits.ibackgroundcopyjob4_getpeercachingflags, bits3_0/IBackgroundCopyJob4::GetPeerCachingFlags
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
 - IBackgroundCopyJob4::GetPeerCachingFlags
 - bits3_0/IBackgroundCopyJob4::GetPeerCachingFlags
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
 - IBackgroundCopyJob4.GetPeerCachingFlags
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

BITS can download from peers only if peercaching is enabled both at the computer level and at the job level; this API affects only the job level. For details, see <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a>.

## -see-also

<a href="/windows/desktop/Bits/group-policies">Group Policies</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyjob4">IBackgroundCopyJob4</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags">IBitsPeerCacheAdministration::GetConfigurationFlags</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags">IBitsPeerCacheAdministration::SetConfigurationFlags</a>