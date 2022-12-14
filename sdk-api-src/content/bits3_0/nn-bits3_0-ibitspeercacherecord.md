---
UID: NN:bits3_0.IBitsPeerCacheRecord
title: IBitsPeerCacheRecord (bits3_0.h)
description: Use IBitsPeerCacheRecord to get information about a file in the cache.
helpviewer_keywords: ["IBitsPeerCacheRecord","IBitsPeerCacheRecord interface [BITS]","IBitsPeerCacheRecord interface [BITS]","described","bits.ibitspeercacherecord","bits3_0/IBitsPeerCacheRecord"]
old-location: bits\ibitspeercacherecord.htm
tech.root: Bits
ms.assetid: 61db33de-a38c-4c52-9f1b-66d46f25c297
ms.date: 12/05/2018
ms.keywords: IBitsPeerCacheRecord, IBitsPeerCacheRecord interface [BITS], IBitsPeerCacheRecord interface [BITS],described, bits.ibitspeercacherecord, bits3_0/IBitsPeerCacheRecord
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
 - IBitsPeerCacheRecord
 - bits3_0/IBitsPeerCacheRecord
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
 - IBitsPeerCacheRecord
---

# IBitsPeerCacheRecord interface


## -description

Use <b>IBitsPeerCacheRecord</b> to get information about a file in the cache. 

To get this interface, call one of the following methods:<ul>
<li>
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-getrecord">IBitsPeerCacheAdministration::GetRecord</a>
</li>
<li>
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-next">IEnumBitsPeerCacheRecords::Next</a>
</li>
</ul>

<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b>IBitsPeerCacheRecord</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitsPeerCacheRecord</b> also has these types of members:

