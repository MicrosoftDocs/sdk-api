---
UID: NF:bits3_0.IEnumBitsPeerCacheRecords.Next
title: IEnumBitsPeerCacheRecords::Next (bits3_0.h)
description: Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.
helpviewer_keywords: ["IEnumBitsPeerCacheRecords interface [BITS]","Next method","IEnumBitsPeerCacheRecords.Next","IEnumBitsPeerCacheRecords::Next","Next","Next method [BITS]","Next method [BITS]","IEnumBitsPeerCacheRecords interface","bits.ienumbitspeercacherecords_next","bits3_0/IEnumBitsPeerCacheRecords::Next"]
old-location: bits\ienumbitspeercacherecords_next.htm
tech.root: Bits
ms.assetid: a8117baa-9f77-4735-bd15-2c7e1e759e9b
ms.date: 12/05/2018
ms.keywords: IEnumBitsPeerCacheRecords interface [BITS],Next method, IEnumBitsPeerCacheRecords.Next, IEnumBitsPeerCacheRecords::Next, Next, Next method [BITS], Next method [BITS],IEnumBitsPeerCacheRecords interface, bits.ienumbitspeercacherecords_next, bits3_0/IEnumBitsPeerCacheRecords::Next
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
 - IEnumBitsPeerCacheRecords::Next
 - bits3_0/IEnumBitsPeerCacheRecords::Next
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
 - IEnumBitsPeerCacheRecords.Next
---

# IEnumBitsPeerCacheRecords::Next


## -description

Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of 
<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a> objects. You must release each object in <i>rgelt</i> when done.

### -param pceltFetched [out]

Number of elements returned in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one. Otherwise, initialize the value of <i>pceltFetched</i> to 0 before calling this method.

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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned less than the number of requested elements.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeercacherecords">IEnumBitsPeerCacheRecords</a>