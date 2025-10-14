---
UID: NF:bits3_0.IEnumBitsPeers.Skip
title: IEnumBitsPeers::Skip (bits3_0.h)
description: Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence. (IEnumBitsPeers.Skip)
helpviewer_keywords: ["IEnumBitsPeers interface [BITS]","Skip method","IEnumBitsPeers.Skip","IEnumBitsPeers::Skip","Skip","Skip method [BITS]","Skip method [BITS]","IEnumBitsPeers interface","bits.ienumbitspeers_skip","bits3_0/IEnumBitsPeers::Skip"]
old-location: bits\ienumbitspeers_skip.htm
tech.root: Bits
ms.assetid: 23a9b424-11a3-4cbf-a867-93026f0725cc
ms.date: 12/05/2018
ms.keywords: IEnumBitsPeers interface [BITS],Skip method, IEnumBitsPeers.Skip, IEnumBitsPeers::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBitsPeers interface, bits.ienumbitspeers_skip, bits3_0/IEnumBitsPeers::Skip
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
 - IEnumBitsPeers::Skip
 - bits3_0/IEnumBitsPeers::Skip
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
 - IEnumBitsPeers.Skip
---

# IEnumBitsPeers::Skip


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

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a>
