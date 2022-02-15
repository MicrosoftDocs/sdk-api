---
UID: NN:bits3_0.IEnumBitsPeers
title: IEnumBitsPeers (bits3_0.h)
description: Use IEnumBitsPeers to enumerate the list of peers that BITS has discovered.
helpviewer_keywords: ["IEnumBitsPeers","IEnumBitsPeers interface [BITS]","IEnumBitsPeers interface [BITS]","described","bits.ienumbitspeers","bits3_0/IEnumBitsPeers"]
old-location: bits\ienumbitspeers.htm
tech.root: Bits
ms.assetid: 2715a58c-ba76-4223-ad9e-453d029e0eda
ms.date: 12/05/2018
ms.keywords: IEnumBitsPeers, IEnumBitsPeers interface [BITS], IEnumBitsPeers interface [BITS],described, bits.ienumbitspeers, bits3_0/IEnumBitsPeers
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
 - IEnumBitsPeers
 - bits3_0/IEnumBitsPeers
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
 - IEnumBitsPeers
---

# IEnumBitsPeers interface


## -description

Use <b>IEnumBitsPeers</b> to enumerate the list of peers that BITS has discovered. 

To get this interface, call the 
<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers">IBitsPeerCacheAdministration::EnumPeers</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b>IEnumBitsPeers</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBitsPeers</b> also has these types of members:

