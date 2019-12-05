---
UID: NN:bits10_1.IBackgroundCopyFile6
title: IBackgroundCopyFile6 (bits10_1.h)
description: Use this interface to request file ranges for On Demand download jobs.
old-location: bits\ibackgroundcopyfile6.htm
tech.root: Bits
ms.assetid: FE3B1BAB-2634-4BE0-91B7-F97041CB3655
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile6, IBackgroundCopyFile6 interface [BITS], IBackgroundCopyFile6 interface [BITS],described, bits.ibackgroundcopyfile6, bits10_1/IBackgroundCopyFile6
ms.topic: interface
f1_keywords:
- bits10_1/IBackgroundCopyFile6
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyFile6 interface


## -description


Use this interface to request file ranges for On Demand download jobs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile6</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bits5_0/nn-bits5_0-ibackgroundcopyfile5">IBackgroundCopyFile5</a>. <b>IBackgroundCopyFile6</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-getfilledfileranges">GetFilledFileRanges</a>
</td>
<td align="left" width="63%">
Returns the set of file ranges that have been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges">RequestFileRanges</a>
</td>
<td align="left" width="63%">
Adds a new set of file ranges to be prioritized for download. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-updatedownloadposition">UpdateDownloadPosition</a>
</td>
<td align="left" width="63%">
Specifies a position to prioritize downloading missing data from.  

</td>
</tr>
</table> 


## -remarks



To get an <b>IBackgroundCopyFile6</b> interface    pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using "__uuidof(IBackgroundCopyFile6)" for the interface identifier.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits4_0/nn-bits4_0-ibackgroundcopyfile4">IBackgroundCopyFile4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits5_0/nn-bits5_0-ibackgroundcopyfile5">IBackgroundCopyFile5</a>
 

 

