---
UID: NF:bits3_0.IBitsPeerCacheAdministration.ClearPeers
title: IBitsPeerCacheAdministration::ClearPeers (bits3_0.h)
description: Removes all peers from the list of peers that can serve content.
helpviewer_keywords: ["ClearPeers","ClearPeers method [BITS]","ClearPeers method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","ClearPeers method","IBitsPeerCacheAdministration.ClearPeers","IBitsPeerCacheAdministration::ClearPeers","bits.ibitspeercacheadministration_clearpeers","bits3_0/IBitsPeerCacheAdministration::ClearPeers"]
old-location: bits\ibitspeercacheadministration_clearpeers.htm
tech.root: Bits
ms.assetid: 79a739ed-7618-410a-a6df-fab11794d932
ms.date: 12/05/2018
ms.keywords: ClearPeers, ClearPeers method [BITS], ClearPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],ClearPeers method, IBitsPeerCacheAdministration.ClearPeers, IBitsPeerCacheAdministration::ClearPeers, bits.ibitspeercacheadministration_clearpeers, bits3_0/IBitsPeerCacheAdministration::ClearPeers
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
 - IBitsPeerCacheAdministration::ClearPeers
 - bits3_0/IBitsPeerCacheAdministration::ClearPeers
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
 - IBitsPeerCacheAdministration.ClearPeers
---

# IBitsPeerCacheAdministration::ClearPeers


## -description

Removes all peers from the list of peers that can serve content.



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

You should not have to call this method.

BITS automatically discovers new peers when a job requests content from a peer. You can also call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-discoverpeers">IBitsPeerCacheAdministration::DiscoverPeers</a> method to force discovery of peers.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-discoverpeers">IBitsPeerCacheAdministration::DiscoverPeers</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers">IBitsPeerCacheAdministration::EnumPeers</a>
