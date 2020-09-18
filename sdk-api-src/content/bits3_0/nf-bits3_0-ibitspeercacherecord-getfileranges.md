---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetFileRanges
title: IBitsPeerCacheRecord::GetFileRanges (bits3_0.h)
description: Gets the ranges of the file that are in the cache.
helpviewer_keywords: ["GetFileRanges","GetFileRanges method [BITS]","GetFileRanges method [BITS]","IBitsPeerCacheRecord interface","IBitsPeerCacheRecord interface [BITS]","GetFileRanges method","IBitsPeerCacheRecord.GetFileRanges","IBitsPeerCacheRecord::GetFileRanges","bits.ibitspeercacherecord_getfileranges","bits3_0/IBitsPeerCacheRecord::GetFileRanges"]
old-location: bits\ibitspeercacherecord_getfileranges.htm
tech.root: Bits
ms.assetid: 63f9821c-f5b6-4646-96e0-4ec61ce16e9b
ms.date: 12/05/2018
ms.keywords: GetFileRanges, GetFileRanges method [BITS], GetFileRanges method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetFileRanges method, IBitsPeerCacheRecord.GetFileRanges, IBitsPeerCacheRecord::GetFileRanges, bits.ibitspeercacherecord_getfileranges, bits3_0/IBitsPeerCacheRecord::GetFileRanges
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
 - IBitsPeerCacheRecord::GetFileRanges
 - bits3_0/IBitsPeerCacheRecord::GetFileRanges
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
 - IBitsPeerCacheRecord.GetFileRanges
---

# IBitsPeerCacheRecord::GetFileRanges


## -description

Gets the ranges of the file that are in the cache.

## -parameters

### -param pRangeCount [out]

Number of elements in <i>ppRanges</i>.

### -param ppRanges [out]

Array of  <a href="/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range">BG_FILE_RANGE</a> structures that specify the ranges of the file that are in the cache. When done, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppRanges</i>.

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
</table>

## -remarks

The method always returns at least one range (for the complete file). Multiple ranges can be returned if the application called <a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges">IBackgroundCopyJob3::AddFileWithRanges</a> to download one or more ranges of a file.

## -see-also

<a href="/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range">BG_FILE_RANGE</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a>