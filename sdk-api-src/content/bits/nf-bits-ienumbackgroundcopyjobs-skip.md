---
UID: NF:bits.IEnumBackgroundCopyJobs.Skip
title: IEnumBackgroundCopyJobs::Skip (bits.h)
description: Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence. (IEnumBackgroundCopyJobs.Skip)
helpviewer_keywords: ["IEnumBackgroundCopyJobs interface [BITS]","Skip method","IEnumBackgroundCopyJobs.Skip","IEnumBackgroundCopyJobs::Skip","Skip","Skip method [BITS]","Skip method [BITS]","IEnumBackgroundCopyJobs interface","_drz_ienumbackgroundcopyjobs_skip","bits.ienumbackgroundcopyjobs_skip","bits/IEnumBackgroundCopyJobs::Skip"]
old-location: bits\ienumbackgroundcopyjobs_skip.htm
tech.root: Bits
ms.assetid: 061f19f7-60e5-4242-871a-cab566c67cad
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyJobs interface [BITS],Skip method, IEnumBackgroundCopyJobs.Skip, IEnumBackgroundCopyJobs::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBackgroundCopyJobs interface, _drz_ienumbackgroundcopyjobs_skip, bits.ienumbackgroundcopyjobs_skip, bits/IEnumBackgroundCopyJobs::Skip
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumBackgroundCopyJobs::Skip
 - bits/IEnumBackgroundCopyJobs::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyJobs.Skip
---

# IEnumBackgroundCopyJobs::Skip


## -description

Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
