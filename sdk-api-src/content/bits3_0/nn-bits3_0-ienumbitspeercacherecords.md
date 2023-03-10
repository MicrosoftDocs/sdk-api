---
UID: NN:bits3_0.IEnumBitsPeerCacheRecords
title: IEnumBitsPeerCacheRecords (bits3_0.h)
description: Use IEnumBitsPeerCacheRecords to enumerate the records of the cache.
helpviewer_keywords: ["IEnumBitsPeerCacheRecords","IEnumBitsPeerCacheRecords interface [BITS]","IEnumBitsPeerCacheRecords interface [BITS]","described","bits.ienumbitspeercacherecords","bits3_0/IEnumBitsPeerCacheRecords"]
old-location: bits\ienumbitspeercacherecords.htm
tech.root: Bits
ms.assetid: 680c1468-d780-44a3-9048-c7c3928234f9
ms.date: 12/05/2018
ms.keywords: IEnumBitsPeerCacheRecords, IEnumBitsPeerCacheRecords interface [BITS], IEnumBitsPeerCacheRecords interface [BITS],described, bits.ienumbitspeercacherecords, bits3_0/IEnumBitsPeerCacheRecords
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
 - IEnumBitsPeerCacheRecords
 - bits3_0/IEnumBitsPeerCacheRecords
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
 - IEnumBitsPeerCacheRecords
---

# IEnumBitsPeerCacheRecords interface


## -description

Use <b>IEnumBitsPeerCacheRecords</b> to enumerate the records of the cache. 

To get this interface, call the 
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords">IBitsPeerCacheAdministration::EnumRecords</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b>IEnumBitsPeerCacheRecords</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBitsPeerCacheRecords</b> also has these types of members:

