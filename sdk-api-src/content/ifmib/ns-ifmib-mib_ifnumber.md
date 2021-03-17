---
UID: NS:ifmib._MIB_IFNUMBER
title: MIB_IFNUMBER (ifmib.h)
description: Stores the number of interfaces on a particular computer.
helpviewer_keywords: ["*PMIB_IFNUMBER","MIB_IFNUMBER","MIB_IFNUMBER structure [MIB]","PMIB_IFNUMBER","PMIB_IFNUMBER structure pointer [MIB]","_mpr_mib_ifnumber","ifmib/MIB_IFNUMBER","ifmib/PMIB_IFNUMBER","iprtrmib/MIB_IFNUMBER","iprtrmib/PMIB_IFNUMBER","mib.mib_ifnumber","rras.mib_ifnumber"]
old-location: mib\mib_ifnumber.htm
tech.root: MIB
ms.assetid: cdab8d39-b0f9-462c-ac5e-ae0c420df067
ms.date: 12/05/2018
ms.keywords: '*PMIB_IFNUMBER, MIB_IFNUMBER, MIB_IFNUMBER structure [MIB], PMIB_IFNUMBER, PMIB_IFNUMBER structure pointer [MIB], _mpr_mib_ifnumber, ifmib/MIB_IFNUMBER, ifmib/PMIB_IFNUMBER, iprtrmib/MIB_IFNUMBER, iprtrmib/PMIB_IFNUMBER, mib.mib_ifnumber, rras.mib_ifnumber'
req.header: ifmib.h
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
req.typenames: MIB_IFNUMBER, *PMIB_IFNUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IFNUMBER
 - ifmib/_MIB_IFNUMBER
 - PMIB_IFNUMBER
 - ifmib/PMIB_IFNUMBER
 - MIB_IFNUMBER
 - ifmib/MIB_IFNUMBER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifmib.h
 - Iprtrmib.h
api_name:
 - MIB_IFNUMBER
---

# MIB_IFNUMBER structure


## -description

The 
<b>MIB_IFNUMBER</b> structure stores the number of interfaces on a particular computer.

## -struct-fields

### -field dwValue

The number of interfaces on the computer.

## -remarks

The <b>MIB_IFNUMBER</b> structure is not currently used. The <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a> and <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a> structures contain a <b>dwNumEntries</b> member that can be used instead of the <b>MIB_IFNUMBER</b> structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IFNUMBER</b> structure is defined in the <i>Ifmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ifmib.h</i> header file is automatically included in <i>Ipmib.h</i> header file. This file is automatically included in the <i>Iprtrmib.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ifmib.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>