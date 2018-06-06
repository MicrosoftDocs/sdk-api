---
UID: NS:iprtrmib.MIB_BOUNDARYROW
title: MIB_BOUNDARYROW
author: windows-sdk-content
description: Contains the IPv4 group address value and mask for a multicast boundary.
old-location: mib\mib_boundaryrow.htm
old-project: MIB
ms.assetid: df252c06-6067-4cf8-b66e-5c9f15e954f5
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_BOUNDARYROW, MIB_BOUNDARYROW, MIB_BOUNDARYROW structure [MIB], PMIB_BOUNDARYROW, PMIB_BOUNDARYROW structure pointer [MIB], iprtrmib/MIB_BOUNDARYROW, iprtrmib/PMIB_BOUNDARYROW, mib.mib_boundaryrow"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MIB_BOUNDARYROW, *PMIB_BOUNDARYROW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_BOUNDARYROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MIB_BOUNDARYROW structure


## -description


The <b>MIB_BOUNDARYROW</b> structure contains the IPv4 group address value and mask for a multicast boundary.


## -struct-fields




### -field dwGroupAddress

The 32-bit integer representation of the IPv4 group address which, when combined with the corresponding value in <b>dwGroupMask</b>, identifies the group range for which the scoped boundary exists. 

<div class="alert"><b>Note</b>  Scoped addresses must come from the range 239.*.*.* as specified in <a href="Http://go.microsoft.com/fwlink/p/?linkid=84040">RFC 2365</a>.</div>
<div> </div>

### -field dwGroupMask

The 32-bit integer representation of the IPv4 group address mask which, when combined with the corresponding value in <b>dwGroupAddress</b>, identifies the group range for which the scoped boundary exists. 


## -remarks



Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.



