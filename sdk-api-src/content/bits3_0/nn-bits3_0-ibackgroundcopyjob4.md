---
UID: NN:bits3_0.IBackgroundCopyJob4
title: IBackgroundCopyJob4
author: windows-driver-content
description: Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.
old-location: bits\ibackgroundcopyjob4.htm
old-project: Bits
ms.assetid: 68909710-f749-487e-b064-9f8630929c53
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IBackgroundCopyJob4, IBackgroundCopyJob4 interface [BITS], IBackgroundCopyJob4 interface [BITS],described, bits.ibackgroundcopyjob4, bits3_0/IBackgroundCopyJob4
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	BitsPrx4.dll
api_name:
-	IBackgroundCopyJob4
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
---

# IBackgroundCopyJob4 interface


## -description


Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob4)</code> as the interface identifier. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob4</b> interface inherits from <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>, <a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a>, and <a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>. <b>IBackgroundCopyJob4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2d258dc4-a6fd-46d7-ac90-2703c8ddc666">GetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Retrieves the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab62c27-5ba1-46f3-a5e9-020fde17a1ef">GetOwnerElevationState</a>
</td>
<td align="left" width="63%">
Get a value that determines if the token of the owner was elevated at the time they created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f5d9576-0948-429b-b136-1b02d7197fcc">GetOwnerIntegrityLevel</a>
</td>
<td align="left" width="63%">
Get the integrity level of the token of the owner that created or took ownership of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b9cdd81-91e8-4d24-a451-61bed51289d4">GetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e29c082-5bd1-465a-8853-aea81a593db6">SetMaximumDownloadTime</a>
</td>
<td align="left" width="63%">
Sets the maximum time that BITS will spend transferring the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">SetPeerCachingFlags</a>
</td>
<td align="left" width="63%">
Sets flags that determine if the files of the job can be cached and served to peers and if BITS can download content for the job from peers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>
 

 

