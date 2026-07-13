---
UID: NS:iprtrmib.MIB_BOUNDARYROW
title: MIB_BOUNDARYROW (iprtrmib.h)
description: Contains the IPv4 group address value and mask for a multicast boundary.
helpviewer_keywords: ["*PMIB_BOUNDARYROW","MIB_BOUNDARYROW","MIB_BOUNDARYROW structure [MIB]","PMIB_BOUNDARYROW","PMIB_BOUNDARYROW structure pointer [MIB]","iprtrmib/MIB_BOUNDARYROW","iprtrmib/PMIB_BOUNDARYROW","mib.mib_boundaryrow"]
old-location: mib\mib_boundaryrow.htm
tech.root: MIB
ms.assetid: df252c06-6067-4cf8-b66e-5c9f15e954f5
ms.date: 12/05/2018
ms.keywords: '*PMIB_BOUNDARYROW, MIB_BOUNDARYROW, MIB_BOUNDARYROW structure [MIB], PMIB_BOUNDARYROW, PMIB_BOUNDARYROW structure pointer [MIB], iprtrmib/MIB_BOUNDARYROW, iprtrmib/PMIB_BOUNDARYROW, mib.mib_boundaryrow'
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_BOUNDARYROW, *PMIB_BOUNDARYROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMIB_BOUNDARYROW
 - iprtrmib/PMIB_BOUNDARYROW
 - MIB_BOUNDARYROW
 - iprtrmib/MIB_BOUNDARYROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_BOUNDARYROW
---

# MIB_BOUNDARYROW structure


## -description

The <b>MIB_BOUNDARYROW</b> structure contains the IPv4 group address value and mask for a multicast boundary.

## -struct-fields

### -field dwGroupAddress

The 32-bit integer representation of the IPv4 group address which, when combined with the corresponding value in <b>dwGroupMask</b>, identifies the group range for which the scoped boundary exists. 

<div class="alert"><b>Note</b>  Scoped addresses must come from the range 239.*.*.* as specified in <a href="https://www.ietf.org/rfc/rfc2365.txt">RFC 2365</a>.</div>
<div> </div>

### -field dwGroupMask

The 32-bit integer representation of the IPv4 group address mask which, when combined with the corresponding value in <b>dwGroupAddress</b>, identifies the group range for which the scoped boundary exists.

## -remarks

Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.

