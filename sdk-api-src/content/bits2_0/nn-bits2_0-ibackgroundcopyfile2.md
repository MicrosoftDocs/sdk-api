---
UID: NN:bits2_0.IBackgroundCopyFile2
title: IBackgroundCopyFile2 (bits2_0.h)
author: windows-sdk-content
description: Use the IBackgroundCopyFile2 interface to specify a new remote name for the file and retrieve the list of ranges to download.
old-location: bits\ibackgroundcopyfile2.htm
tech.root: Bits
ms.assetid: facff24d-56a3-4a1f-a726-3442c17fe869
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile2, IBackgroundCopyFile2 interface [BITS], IBackgroundCopyFile2 interface [BITS],described, bits.ibackgroundcopyfile2, bits2_0/IBackgroundCopyFile2
ms.topic: interface
f1_keywords: 
 - "bits2_0/IBackgroundCopyFile2"
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003, and  Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyFile2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyFile2 interface


## -description


Use the 
<b>IBackgroundCopyFile2</b> interface to specify a new remote name  for the file and retrieve the list of ranges to download.

The 
<b>IBackgroundCopyFile2</b> interface inherits from the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> interface. 

To get an 
<b>IBackgroundCopyFile2</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile2) for the interface identifier. Use the 
<b>IBackgroundCopyFile2</b> interface pointer to call both the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> and 
<b>IBackgroundCopyFile2</b> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>. <b>IBackgroundCopyFile2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-getfileranges">GetFileRanges</a>
</td>
<td align="left" width="63%">
Retrieves the array of ranges that you want to download from the URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename">SetRemoteName</a>
</td>
<td align="left" width="63%">
Changes the remote name to a new URL.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>
 

 

