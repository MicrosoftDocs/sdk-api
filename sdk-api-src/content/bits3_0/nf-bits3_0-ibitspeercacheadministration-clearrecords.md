---
UID: NF:bits3_0.IBitsPeerCacheAdministration.ClearRecords
title: IBitsPeerCacheAdministration::ClearRecords (bits3_0.h)
description: Removes all the records and files from the cache.
helpviewer_keywords: ["ClearRecords","ClearRecords method [BITS]","ClearRecords method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","ClearRecords method","IBitsPeerCacheAdministration.ClearRecords","IBitsPeerCacheAdministration::ClearRecords","bits.ibitspeercacheadministration_clearrecords","bits3_0/IBitsPeerCacheAdministration::ClearRecords"]
old-location: bits\ibitspeercacheadministration_clearrecords.htm
tech.root: Bits
ms.assetid: 96e18c5d-6c76-4953-8e8e-3e98943478d8
ms.date: 12/05/2018
ms.keywords: ClearRecords, ClearRecords method [BITS], ClearRecords method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],ClearRecords method, IBitsPeerCacheAdministration.ClearRecords, IBitsPeerCacheAdministration::ClearRecords, bits.ibitspeercacheadministration_clearrecords, bits3_0/IBitsPeerCacheAdministration::ClearRecords
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
 - IBitsPeerCacheAdministration::ClearRecords
 - bits3_0/IBitsPeerCacheAdministration::ClearRecords
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
 - IBitsPeerCacheAdministration.ClearRecords
---

# IBitsPeerCacheAdministration::ClearRecords


## -description

Removes all the records and files from the cache.



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

The cache is not cleared until all current cache activity is complete.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-deleterecord">IBitsPeerCacheAdministration::DeleteRecord</a>
