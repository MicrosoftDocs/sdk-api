---
UID: NS:ipmib._MIB_IPFORWARDNUMBER
title: MIB_IPFORWARDNUMBER (ipmib.h)
description: Stores the number of routes in a particular IP routing table.
helpviewer_keywords: ["*PMIB_IPFORWARDNUMBER","MIB_IPFORWARDNUMBER","MIB_IPFORWARDNUMBER structure [MIB]","PMIB_IPFORWARDNUMBER","PMIB_IPFORWARDNUMBER structure pointer [MIB]","_mpr_mib_ipforwardnumber","ipmib/MIB_IPFORWARDNUMBER","ipmib/PMIB_IPFORWARDNUMBER","iprtrmib/MIB_IPFORWARDNUMBER","iprtrmib/PMIB_IPFORWARDNUMBER","mib.mib_ipforwardnumber","rras.mib_ipforwardnumber"]
old-location: mib\mib_ipforwardnumber.htm
tech.root: MIB
ms.assetid: 71508d8e-3265-4c08-913c-248af2d8bbd6
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPFORWARDNUMBER, MIB_IPFORWARDNUMBER, MIB_IPFORWARDNUMBER structure [MIB], PMIB_IPFORWARDNUMBER, PMIB_IPFORWARDNUMBER structure pointer [MIB], _mpr_mib_ipforwardnumber, ipmib/MIB_IPFORWARDNUMBER, ipmib/PMIB_IPFORWARDNUMBER, iprtrmib/MIB_IPFORWARDNUMBER, iprtrmib/PMIB_IPFORWARDNUMBER, mib.mib_ipforwardnumber, rras.mib_ipforwardnumber'
req.header: ipmib.h
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
req.typenames: MIB_IPFORWARDNUMBER, *PMIB_IPFORWARDNUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPFORWARDNUMBER
 - ipmib/_MIB_IPFORWARDNUMBER
 - PMIB_IPFORWARDNUMBER
 - ipmib/PMIB_IPFORWARDNUMBER
 - MIB_IPFORWARDNUMBER
 - ipmib/MIB_IPFORWARDNUMBER
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
 - MIB_IPFORWARDNUMBER
---

# MIB_IPFORWARDNUMBER structure


## -description

The 
<b>MIB_IPFORWARDNUMBER</b> structure stores the number of routes in a particular IP routing table.

## -struct-fields

### -field dwValue

Specifies the number of routes in the IP routing table.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a>