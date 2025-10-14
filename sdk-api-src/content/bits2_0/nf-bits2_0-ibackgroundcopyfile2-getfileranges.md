---
UID: NF:bits2_0.IBackgroundCopyFile2.GetFileRanges
title: IBackgroundCopyFile2::GetFileRanges (bits2_0.h)
description: Retrieves the ranges that you want to download from the remote file.
helpviewer_keywords: ["GetFileRanges","GetFileRanges method [BITS]","GetFileRanges method [BITS]","IBackgroundCopyFile2 interface","IBackgroundCopyFile2 interface [BITS]","GetFileRanges method","IBackgroundCopyFile2.GetFileRanges","IBackgroundCopyFile2::GetFileRanges","bits.ibackgroundcopyfile2_getfileranges","bits2_0/IBackgroundCopyFile2::GetFileRanges"]
old-location: bits\ibackgroundcopyfile2_getfileranges.htm
tech.root: Bits
ms.assetid: 2e0ea08e-5f97-45c9-9280-ce6c4dce7a17
ms.date: 12/05/2018
ms.keywords: GetFileRanges, GetFileRanges method [BITS], GetFileRanges method [BITS],IBackgroundCopyFile2 interface, IBackgroundCopyFile2 interface [BITS],GetFileRanges method, IBackgroundCopyFile2.GetFileRanges, IBackgroundCopyFile2::GetFileRanges, bits.ibackgroundcopyfile2_getfileranges, bits2_0/IBackgroundCopyFile2::GetFileRanges
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003,  and Windows XP
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile2::GetFileRanges
 - bits2_0/IBackgroundCopyFile2::GetFileRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyFile2.GetFileRanges
---

# IBackgroundCopyFile2::GetFileRanges


## -description

Retrieves the ranges that you want to download from the remote file.

## -parameters

### -param RangeCount [in, out]

Number of elements in <i>Ranges</i>.

### -param Ranges [out]

Array of  <a href="/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range">BG_FILE_RANGE</a> structures that specify the ranges to download. When done, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>Ranges</i>.

## -returns

This method returns the following return values, as well as others.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No ranges were specified or the job is an upload or upload-reply job. <i>RangeCount</i> is set to zero and <i>Ranges</i> is set to <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range">BG_FILE_RANGE</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges">IBackgroundCopyJob3::AddFileWithRanges</a>