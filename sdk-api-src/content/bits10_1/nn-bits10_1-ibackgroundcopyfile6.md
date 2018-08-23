---
UID: NN:bits10_1.IBackgroundCopyFile6
title: IBackgroundCopyFile6
author: windows-sdk-content
description: Use this interface to request file ranges for On Demand download jobs.
old-location: bits\ibackgroundcopyfile6.htm
old-project: bits
ms.assetid: FE3B1BAB-2634-4BE0-91B7-F97041CB3655
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyFile6, IBackgroundCopyFile6 interface [BITS], IBackgroundCopyFile6 interface [BITS],described, bits.ibackgroundcopyfile6, bits10_1/IBackgroundCopyFile6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bits10_1.h
req.include-header: Bits10_0.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_TIMES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bits10_1.h
api_name:
 - IBackgroundCopyFile6
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyFile6 interface


## -description


Use this interface to request file ranges for On Demand download jobs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile6</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Mt147017(v=VS.85).aspx">IBackgroundCopyFile5</a>. <b>IBackgroundCopyFile6</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492764(v=VS.85).aspx">GetFilledFileRanges</a>
</td>
<td align="left" width="63%">
Returns the set of file ranges that have been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492766(v=VS.85).aspx">RequestFileRanges</a>
</td>
<td align="left" width="63%">
Adds a new set of file ranges to be prioritized for download. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492767(v=VS.85).aspx">UpdateDownloadPosition</a>
</td>
<td align="left" width="63%">
Specifies a position to prioritize downloading missing data from.  

</td>
</tr>
</table> 


## -remarks



To get an <b>IBackgroundCopyFile6</b> interface    pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using "__uuidof(IBackgroundCopyFile6)" for the interface identifier.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362881(v=VS.85).aspx">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362944(v=VS.85).aspx">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362952(v=VS.85).aspx">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd904468(v=VS.85).aspx">IBackgroundCopyFile4</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt147017(v=VS.85).aspx">IBackgroundCopyFile5</a>
 

 

