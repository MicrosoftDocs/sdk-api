---
UID: NN:bits10_1.IBackgroundCopyFile6
title: IBackgroundCopyFile6
author: windows-sdk-content
description: Use this interface to request file ranges for On Demand download jobs.
old-location: bits\ibackgroundcopyfile6.htm
tech.root: bits
ms.assetid: FE3B1BAB-2634-4BE0-91B7-F97041CB3655
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyFile6, IBackgroundCopyFile6 interface [BITS], IBackgroundCopyFile6 interface [BITS],described, bits.ibackgroundcopyfile6, bits10_1/IBackgroundCopyFile6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bits10_1.h
req.include-header: Bits10_0.h
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile6 interface


## -description


Use this interface to request file ranges for On Demand download jobs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile6</b> interface inherits from <a href="https://msdn.microsoft.com/548b507a-4874-4ccf-829e-13e1ca6cc958">IBackgroundCopyFile5</a>. <b>IBackgroundCopyFile6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/D3549C42-6642-4C3C-9D97-6F2F9732C48E">GetFilledFileRanges</a>
</td>
<td align="left" width="63%">
Returns the set of file ranges that have been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C36BDE94-03AC-4F06-B17B-B8729226F8AC">RequestFileRanges</a>
</td>
<td align="left" width="63%">
Adds a new set of file ranges to be prioritized for download. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/243F9D5A-32D8-4D39-A9B2-E452CF745844">UpdateDownloadPosition</a>
</td>
<td align="left" width="63%">
Specifies a position to prioritize downloading missing data from.  

</td>
</tr>
</table> 


## -remarks



To get an <b>IBackgroundCopyFile6</b> interface    pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using "__uuidof(IBackgroundCopyFile6)" for the interface identifier.





## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/facff24d-56a3-4a1f-a726-3442c17fe869">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/d404c4f8-cc97-4254-bca8-41bc359f0777">IBackgroundCopyFile4</a>



<a href="https://msdn.microsoft.com/548b507a-4874-4ccf-829e-13e1ca6cc958">IBackgroundCopyFile5</a>
 

 

