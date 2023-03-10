---
UID: NS:ipmib._MIB_IPADDRTABLE
title: MIB_IPADDRTABLE (ipmib.h)
description: Contains a table of IPv4 address entries.
helpviewer_keywords: ["*PMIB_IPADDRTABLE","MIB_IPADDRTABLE","MIB_IPADDRTABLE structure [MIB]","PMIB_IPADDRTABLE","PMIB_IPADDRTABLE structure pointer [MIB]","_mpr_mib_ipaddrtable","ipmib/MIB_IPADDRTABLE","ipmib/PMIB_IPADDRTABLE","iprtrmib/MIB_IPADDRTABLE","iprtrmib/PMIB_IPADDRTABLE","mib.mib_ipaddrtable","rras.mib_ipaddrtable"]
old-location: mib\mib_ipaddrtable.htm
tech.root: MIB
ms.assetid: 12a929e5-813d-4dae-9ea0-5a3c0a88cf05
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPADDRTABLE, MIB_IPADDRTABLE, MIB_IPADDRTABLE structure [MIB], PMIB_IPADDRTABLE, PMIB_IPADDRTABLE structure pointer [MIB], _mpr_mib_ipaddrtable, ipmib/MIB_IPADDRTABLE, ipmib/PMIB_IPADDRTABLE, iprtrmib/MIB_IPADDRTABLE, iprtrmib/PMIB_IPADDRTABLE, mib.mib_ipaddrtable, rras.mib_ipaddrtable'
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
req.typenames: MIB_IPADDRTABLE, *PMIB_IPADDRTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPADDRTABLE
 - ipmib/_MIB_IPADDRTABLE
 - PMIB_IPADDRTABLE
 - ipmib/PMIB_IPADDRTABLE
 - MIB_IPADDRTABLE
 - ipmib/MIB_IPADDRTABLE
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
 - MIB_IPADDRTABLE
---

# MIB_IPADDRTABLE structure


## -description

The 
<b>MIB_IPADDRTABLE</b> structure contains a table of IPv4 address entries.

## -struct-fields

### -field dwNumEntries

The number of IPv4 address entries in the table.

### -field table

A pointer to a table of IPv4 address entries implemented as an array of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrrow_w2k">MIB_IPADDRROW</a> structures.

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function retrieves the interface–to–IPv4 address mapping table on a local computer and returns this information in an <b>MIB_IPADDRTABLE</b> structure.

The <b>MIB_IPADDRTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrrow_w2k">MIB_IPADDRROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IPADDRROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IPADDRROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrrow_w2k">MIB_IPADDRROW</a> is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.



#### Examples

To view an example that retrieves the <b>MIB_IPADDRTABLE</b> structure and then prints out the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrrow_w2k">MIB_IPADDRROW</a> structures in this table, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrrow_w2k">MIB_IPADDRROW</a>