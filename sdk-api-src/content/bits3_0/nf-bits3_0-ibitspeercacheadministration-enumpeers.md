---
UID: NF:bits3_0.IBitsPeerCacheAdministration.EnumPeers
title: IBitsPeerCacheAdministration::EnumPeers (bits3_0.h)
description: Gets an IEnumBitsPeers interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.
helpviewer_keywords: ["EnumPeers","EnumPeers method [BITS]","EnumPeers method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","EnumPeers method","IBitsPeerCacheAdministration.EnumPeers","IBitsPeerCacheAdministration::EnumPeers","bits.ibitspeercacheadministration_enumpeers","bits3_0/IBitsPeerCacheAdministration::EnumPeers"]
old-location: bits\ibitspeercacheadministration_enumpeers.htm
tech.root: Bits
ms.assetid: 8786d7d8-9ffb-4492-9834-90b97f97e4cf
ms.date: 12/05/2018
ms.keywords: EnumPeers, EnumPeers method [BITS], EnumPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],EnumPeers method, IBitsPeerCacheAdministration.EnumPeers, IBitsPeerCacheAdministration::EnumPeers, bits.ibitspeercacheadministration_enumpeers, bits3_0/IBitsPeerCacheAdministration::EnumPeers
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
 - IBitsPeerCacheAdministration::EnumPeers
 - bits3_0/IBitsPeerCacheAdministration::EnumPeers
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
 - IBitsPeerCacheAdministration.EnumPeers
---

# IBitsPeerCacheAdministration::EnumPeers


## -description

Gets an <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.

## -parameters

### -param ppEnum [out]

An <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. Release <i>ppEnum</i> when done.

## -returns

This method returns S_OK on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-clearpeers">IBitsPeerCacheAdministration::ClearPeers</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-discoverpeers">IBitsPeerCacheAdministration::DiscoverPeers</a>