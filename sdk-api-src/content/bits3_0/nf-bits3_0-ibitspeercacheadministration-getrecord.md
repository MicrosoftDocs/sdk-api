---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetRecord
title: IBitsPeerCacheAdministration::GetRecord (bits3_0.h)
description: Gets a record from the cache.
helpviewer_keywords: ["GetRecord","GetRecord method [BITS]","GetRecord method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","GetRecord method","IBitsPeerCacheAdministration.GetRecord","IBitsPeerCacheAdministration::GetRecord","bits.ibitspeercacheadministration_getrecord","bits3_0/IBitsPeerCacheAdministration::GetRecord"]
old-location: bits\ibitspeercacheadministration_getrecord.htm
tech.root: Bits
ms.assetid: 7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c
ms.date: 12/05/2018
ms.keywords: GetRecord, GetRecord method [BITS], GetRecord method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetRecord method, IBitsPeerCacheAdministration.GetRecord, IBitsPeerCacheAdministration::GetRecord, bits.ibitspeercacheadministration_getrecord, bits3_0/IBitsPeerCacheAdministration::GetRecord
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
 - IBitsPeerCacheAdministration::GetRecord
 - bits3_0/IBitsPeerCacheAdministration::GetRecord
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
 - IBitsPeerCacheAdministration.GetRecord
---

# IBitsPeerCacheAdministration::GetRecord


## -description

Gets a record from the cache.

## -parameters

### -param id [in]

Identifier of the record to get from the cache. The <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacherecord-getid">IBitsPeerCacheRecord::GetId</a> method returns the identifier.

### -param ppRecord [out]

An <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a> interface of the cache record. Release <i>ppRecord</i> when done.

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

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-deleterecord">IBitsPeerCacheAdministration::DeleteRecord</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords">IBitsPeerCacheAdministration::EnumRecords</a>