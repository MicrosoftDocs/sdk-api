---
UID: NS:ifmib._MIB_IFTABLE
title: MIB_IFTABLE (ifmib.h)
description: Contains a table of interface entries.
helpviewer_keywords: ["*PMIB_IFTABLE","MIB_IFTABLE","MIB_IFTABLE structure [MIB]","PMIB_IFTABLE","PMIB_IFTABLE structure pointer [MIB]","_mpr_mib_iftable","ifmib/MIB_IFTABLE","ifmib/PMIB_IFTABLE","iprtrmib/MIB_IFTABLE","iprtrmib/PMIB_IFTABLE","mib.mib_iftable","rras.mib_iftable"]
old-location: mib\mib_iftable.htm
tech.root: MIB
ms.assetid: 7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7
ms.date: 12/05/2018
ms.keywords: '*PMIB_IFTABLE, MIB_IFTABLE, MIB_IFTABLE structure [MIB], PMIB_IFTABLE, PMIB_IFTABLE structure pointer [MIB], _mpr_mib_iftable, ifmib/MIB_IFTABLE, ifmib/PMIB_IFTABLE, iprtrmib/MIB_IFTABLE, iprtrmib/PMIB_IFTABLE, mib.mib_iftable, rras.mib_iftable'
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
req.typenames: MIB_IFTABLE, *PMIB_IFTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IFTABLE
 - ifmib/_MIB_IFTABLE
 - PMIB_IFTABLE
 - ifmib/PMIB_IFTABLE
 - MIB_IFTABLE
 - ifmib/MIB_IFTABLE
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
 - MIB_IFTABLE
---

# MIB_IFTABLE structure


## -description

The 
<b>MIB_IFTABLE</b> structure contains a table of interface entries.

## -struct-fields

### -field dwNumEntries

The number of interface entries in the array.

### -field table

An array of 
<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> structures containing interface entries.

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiftable">GetIfTable</a> function enumerates the interface entries on a local system and returns this information in a <b>MIB_IFTABLE</b> structure. 



The <b>MIB_IFTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IFROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IFROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IFTABLE</b> structure is defined in the <i>Ifmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ifmib.h</i> header file is automatically included in <i>Ipmib.h</i> header file. This file is automatically included in the <i>Iprtrmib.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ifmib.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiftable">GetIfTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifnumber">MIB_IFNUMBER</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>