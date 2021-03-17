---
UID: NS:iprtrmib._MIB_BEST_IF
title: MIB_BEST_IF (iprtrmib.h)
description: Stores the index of the interface that has the best route to a particular destination IPv4 address.
helpviewer_keywords: ["*PMIB_BEST_IF","MIB_BEST_IF","MIB_BEST_IF structure [MIB]","PMIB_BEST_IF","PMIB_BEST_IF structure pointer [MIB]","_mpr_mib_best_if","ipmib/MIB_BEST_IF","ipmib/PMIB_BEST_IF","iprtrmib/MIB_BEST_IF","iprtrmib/PMIB_BEST_IF","mib.mib_best_if","rras.mib_best_if"]
old-location: mib\mib_best_if.htm
tech.root: MIB
ms.assetid: a557acfe-c5c6-44fc-b1f1-2aa7ef599d44
ms.date: 12/05/2018
ms.keywords: '*PMIB_BEST_IF, MIB_BEST_IF, MIB_BEST_IF structure [MIB], PMIB_BEST_IF, PMIB_BEST_IF structure pointer [MIB], _mpr_mib_best_if, ipmib/MIB_BEST_IF, ipmib/PMIB_BEST_IF, iprtrmib/MIB_BEST_IF, iprtrmib/PMIB_BEST_IF, mib.mib_best_if, rras.mib_best_if'
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_BEST_IF, *PMIB_BEST_IF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_BEST_IF
 - iprtrmib/_MIB_BEST_IF
 - PMIB_BEST_IF
 - iprtrmib/PMIB_BEST_IF
 - MIB_BEST_IF
 - iprtrmib/MIB_BEST_IF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_BEST_IF
---

# MIB_BEST_IF structure


## -description

The 
<b>MIB_BEST_IF</b> structure stores the index of the interface that has the best route to a particular destination IPv4 address.

## -struct-fields

### -field dwDestAddr

Specifies the IPv4 address of the destination.

### -field dwIfIndex

Specifies the index of the interface that has the best route to the destination address specified by the <b>dwDestAddr</b> member.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_BEST_IF</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestroute">GetBestRoute</a>