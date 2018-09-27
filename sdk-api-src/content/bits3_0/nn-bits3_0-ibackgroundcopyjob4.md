---
UID: NN:bits3_0.IBackgroundCopyJob4
title: IBackgroundCopyJob4
author: windows-sdk-content
description: Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.
old-location: bits\ibackgroundcopyjob4.htm
tech.root: Bits
ms.assetid: 68909710-f749-487e-b064-9f8630929c53
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IBackgroundCopyJob4, IBackgroundCopyJob4 interface [BITS], IBackgroundCopyJob4 interface [BITS],described, bits.ibackgroundcopyjob4, bits3_0/IBackgroundCopyJob4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx4.dll
api_name:
 - IBackgroundCopyJob4
product: Windows
targetos: Windows
req.typenames: 
req.redist: BITS 2.5 on  Windows Server 2003,  Windows XP
---

# IBackgroundCopyJob4 interface


## -description


Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob4)</code> as the interface identifier. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob4</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa362990(v=VS.85).aspx">IBackgroundCopyJob3</a>. <b>IBackgroundCopyJob4</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa964244(v=VS.85).aspx">GetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Retrieves the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964245(v=VS.85).aspx">GetOwnerElevationState</a>
</td>
<td align="left" width="63%">
Get a value that determines if the token of the owner was elevated at the time they created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964246(v=VS.85).aspx">GetOwnerIntegrityLevel</a>
</td>
<td align="left" width="63%">
Get the integrity level of the token of the owner that created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964247(v=VS.85).aspx">GetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964248(v=VS.85).aspx">SetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Sets the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964249(v=VS.85).aspx">SetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Sets flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362990(v=VS.85).aspx">IBackgroundCopyJob3</a>
 

 

