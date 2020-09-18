---
UID: NF:bits3_0.IBitsPeerCacheAdministration.EnumRecords
title: IBitsPeerCacheAdministration::EnumRecords (bits3_0.h)
description: Gets an IEnumBitsPeerCacheRecords interface pointer that you use to enumerate the records in the cache. The enumeration is a snapshot of the records in the cache.
helpviewer_keywords: ["EnumRecords","EnumRecords method [BITS]","EnumRecords method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","EnumRecords method","IBitsPeerCacheAdministration.EnumRecords","IBitsPeerCacheAdministration::EnumRecords","bits.ibitspeercacheadministration_enumrecords","bits3_0/IBitsPeerCacheAdministration::EnumRecords"]
old-location: bits\ibitspeercacheadministration_enumrecords.htm
tech.root: Bits
ms.assetid: b471cee0-0ad0-4488-9819-e524e50dbc76
ms.date: 12/05/2018
ms.keywords: EnumRecords, EnumRecords method [BITS], EnumRecords method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],EnumRecords method, IBitsPeerCacheAdministration.EnumRecords, IBitsPeerCacheAdministration::EnumRecords, bits.ibitspeercacheadministration_enumrecords, bits3_0/IBitsPeerCacheAdministration::EnumRecords
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
 - IBitsPeerCacheAdministration::EnumRecords
 - bits3_0/IBitsPeerCacheAdministration::EnumRecords
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
 - IBitsPeerCacheAdministration.EnumRecords
---

# IBitsPeerCacheAdministration::EnumRecords


## -description

Gets an <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeercacherecords">IEnumBitsPeerCacheRecords</a> interface pointer that you use to enumerate the records in the cache. The enumeration is a snapshot of the records in the cache.

## -parameters

### -param ppEnum [out]

An <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeercacherecords">IEnumBitsPeerCacheRecords</a> interface pointer that you use to enumerate the records in the cache. Release <i>ppEnum</i> when done.

## -returns

This method returns S_OK on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-clearpeers">IBitsPeerCacheAdministration::ClearPeers</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-getrecord">IBitsPeerCacheAdministration::GetRecord</a>