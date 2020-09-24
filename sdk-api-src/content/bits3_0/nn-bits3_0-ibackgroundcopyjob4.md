---
UID: NN:bits3_0.IBackgroundCopyJob4
title: IBackgroundCopyJob4 (bits3_0.h)
description: Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.
helpviewer_keywords: ["IBackgroundCopyJob4","IBackgroundCopyJob4 interface [BITS]","IBackgroundCopyJob4 interface [BITS]","described","bits.ibackgroundcopyjob4","bits3_0/IBackgroundCopyJob4"]
old-location: bits\ibackgroundcopyjob4.htm
tech.root: Bits
ms.assetid: 68909710-f749-487e-b064-9f8630929c53
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob4, IBackgroundCopyJob4 interface [BITS], IBackgroundCopyJob4 interface [BITS],described, bits.ibackgroundcopyjob4, bits3_0/IBackgroundCopyJob4
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
req.dll: BitsPrx4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 2.5 on  Windows Server 2003,  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob4
 - bits3_0/IBackgroundCopyJob4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx4.dll
api_name:
 - IBackgroundCopyJob4
---

# IBackgroundCopyJob4 interface


## -description

Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob4)</code> as the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob4</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>, <a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>, and <a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>. <b>IBackgroundCopyJob4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-getmaximumdownloadtime">GetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Retrieves the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate">GetOwnerElevationState</a>
</td>
<td align="left" width="63%">
Get a value that determines if the token of the owner was elevated at the time they created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel">GetOwnerIntegrityLevel</a>
</td>
<td align="left" width="63%">
Get the integrity level of the token of the owner that created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-getpeercachingflags">GetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime">SetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Sets the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">SetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Sets flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>