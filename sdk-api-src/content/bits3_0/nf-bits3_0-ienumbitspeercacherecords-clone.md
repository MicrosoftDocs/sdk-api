---
UID: NF:bits3_0.IEnumBitsPeerCacheRecords.Clone
title: IEnumBitsPeerCacheRecords::Clone (bits3_0.h)
description: Creates another IEnumBitsPeerCacheRecords enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBitsPeerCacheRecords interface","IEnumBitsPeerCacheRecords interface [BITS]","Clone method","IEnumBitsPeerCacheRecords.Clone","IEnumBitsPeerCacheRecords::Clone","bits.ienumbitspeercacherecords_clone","bits3_0/IEnumBitsPeerCacheRecords::Clone"]
old-location: bits\ienumbitspeercacherecords_clone.htm
tech.root: Bits
ms.assetid: 4eb19401-119d-4ce6-92b1-aa41b6dcb97c
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBitsPeerCacheRecords interface, IEnumBitsPeerCacheRecords interface [BITS],Clone method, IEnumBitsPeerCacheRecords.Clone, IEnumBitsPeerCacheRecords::Clone, bits.ienumbitspeercacherecords_clone, bits3_0/IEnumBitsPeerCacheRecords::Clone
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
 - IEnumBitsPeerCacheRecords::Clone
 - bits3_0/IEnumBitsPeerCacheRecords::Clone
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
 - IEnumBitsPeerCacheRecords.Clone
---

# IEnumBitsPeerCacheRecords::Clone


## -description

Creates another 
<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeercacherecords">IEnumBitsPeerCacheRecords</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -parameters

### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnum</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeercacherecords">IEnumBitsPeerCacheRecords</a>