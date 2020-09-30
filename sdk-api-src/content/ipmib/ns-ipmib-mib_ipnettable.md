---
UID: NS:ipmib._MIB_IPNETTABLE
title: MIB_IPNETTABLE (ipmib.h)
description: Contains a table of Address Resolution Protocol (ARP) entries for IPv4 addresses.
helpviewer_keywords: ["*PMIB_IPNETTABLE","MIB_IPNETTABLE","MIB_IPNETTABLE structure [MIB]","PMIB_IPNETTABLE","PMIB_IPNETTABLE structure pointer [MIB]","_mpr_mib_ipnettable","ipmib/MIB_IPNETTABLE","ipmib/PMIB_IPNETTABLE","iprtrmib/MIB_IPNETTABLE","iprtrmib/PMIB_IPNETTABLE","mib.mib_ipnettable","rras.mib_ipnettable"]
old-location: mib\mib_ipnettable.htm
tech.root: MIB
ms.assetid: 1cac1c19-bc42-4aee-b9d0-d007b8798eeb
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPNETTABLE, MIB_IPNETTABLE, MIB_IPNETTABLE structure [MIB], PMIB_IPNETTABLE, PMIB_IPNETTABLE structure pointer [MIB], _mpr_mib_ipnettable, ipmib/MIB_IPNETTABLE, ipmib/PMIB_IPNETTABLE, iprtrmib/MIB_IPNETTABLE, iprtrmib/PMIB_IPNETTABLE, mib.mib_ipnettable, rras.mib_ipnettable'
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
req.typenames: MIB_IPNETTABLE, *PMIB_IPNETTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPNETTABLE
 - ipmib/_MIB_IPNETTABLE
 - PMIB_IPNETTABLE
 - ipmib/PMIB_IPNETTABLE
 - MIB_IPNETTABLE
 - ipmib/MIB_IPNETTABLE
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
 - MIB_IPNETTABLE
---

# MIB_IPNETTABLE structure


## -description

The 
<b>MIB_IPNETTABLE</b> structure contains a table of Address Resolution Protocol (ARP) entries for IPv4 addresses.

## -struct-fields

### -field dwNumEntries

The number of ARP entries in the table.

### -field table

A pointer to a table of ARP entries implemented as an array of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a> structures.

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a> function retrieves the IPv4-to-physical address mapping table.


on a local system and returns this information in a <b>MIB_IPNETTABLE</b> structure. 



The <b>dwNumEntries</b> member in this structure may be zero if there are no ARP entries in the table.

The <b>MIB_IPNETTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IPNETROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IPNETROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IPNETTABLE</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a>