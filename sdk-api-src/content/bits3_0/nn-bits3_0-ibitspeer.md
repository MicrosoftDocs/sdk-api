---
UID: NN:bits3_0.IBitsPeer
title: IBitsPeer (bits3_0.h)
description: Use IBitsPeer to get information about a peer in the neighborhood.
helpviewer_keywords: ["IBitsPeer","IBitsPeer interface [BITS]","IBitsPeer interface [BITS]","described","bits.ibitspeer","bits3_0/IBitsPeer"]
old-location: bits\ibitspeer.htm
tech.root: Bits
ms.assetid: 617b88d4-6c3e-4c33-9bfa-6d9f6f629866
ms.date: 12/05/2018
ms.keywords: IBitsPeer, IBitsPeer interface [BITS], IBitsPeer interface [BITS],described, bits.ibitspeer, bits3_0/IBitsPeer
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
 - IBitsPeer
 - bits3_0/IBitsPeer
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
 - IBitsPeer
---

# IBitsPeer interface


## -description

Use <b>IBitsPeer</b> to get information about a peer in the neighborhood. 

To get this  interface, call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeers-next">IEnumBitsPeers::Next</a> method. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b>IBitsPeer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitsPeer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a>
