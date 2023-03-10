---
UID: NS:ipmib._MIB_IPADDRROW_XP
title: MIB_IPADDRROW_XP (ipmib.h)
description: MIB_IPADDRROW_XP (ipmib.h) specifies information for a particular IPv4 address in the MIB_IPADDRTABLE structure.
helpviewer_keywords: ["*PMIB_IPADDRROW","*PMIB_IPADDRROW_XP","MIB_IPADDRROW","MIB_IPADDRROW structure [MIB]","MIB_IPADDRROW_XP","MIB_IPADDR_DELETED","MIB_IPADDR_DISCONNECTED","MIB_IPADDR_DYNAMIC","MIB_IPADDR_PRIMARY","MIB_IPADDR_TRANSIENT","PMIB_IPADDRROW","PMIB_IPADDRROW structure pointer [MIB]","_mpr_mib_ipaddrrow","ipmib/MIB_IPADDRROW","ipmib/PMIB_IPADDRROW","iprtrmib/MIB_IPADDRROW","iprtrmib/PMIB_IPADDRROW","mib.mib_ipaddrrow","rras.mib_ipaddrrow"]
old-location: mib\mib_ipaddrrow.htm
tech.root: MIB
ms.assetid: ed1777bd-4c02-43e0-9bbb-6bb02702e1a4
ms.date: 08/03/2022
ms.keywords: '*PMIB_IPADDRROW, *PMIB_IPADDRROW_XP, MIB_IPADDRROW, MIB_IPADDRROW structure [MIB], MIB_IPADDRROW_XP, MIB_IPADDR_DELETED, MIB_IPADDR_DISCONNECTED, MIB_IPADDR_DYNAMIC, MIB_IPADDR_PRIMARY, MIB_IPADDR_TRANSIENT, PMIB_IPADDRROW, PMIB_IPADDRROW structure pointer [MIB], _mpr_mib_ipaddrrow, ipmib/MIB_IPADDRROW, ipmib/PMIB_IPADDRROW, iprtrmib/MIB_IPADDRROW, iprtrmib/PMIB_IPADDRROW, mib.mib_ipaddrrow, rras.mib_ipaddrrow'
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
req.typenames: MIB_IPADDRROW_XP, *PMIB_IPADDRROW_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPADDRROW_XP
 - ipmib/_MIB_IPADDRROW_XP
 - PMIB_IPADDRROW_XP
 - ipmib/PMIB_IPADDRROW_XP
 - MIB_IPADDRROW_XP
 - ipmib/MIB_IPADDRROW_XP
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
 - MIB_IPADDRROW
---

## -description

The 
<b>MIB_IPADDRROW</b> specifies information for a particular IPv4 address in the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a> structure.

## -struct-fields

### -field dwAddr

Type: <b>DWORD</b>

The IPv4 address in network byte order.

### -field dwIndex

Type: <b>DWORD</b>

The index of the interface associated with this IPv4 address.

### -field dwMask

Type: <b>DWORD</b>

The subnet mask for the IPv4 address in network byte order.

### -field dwBCastAddr

Type: <b>DWORD</b>

The broadcast address in network byte order. A broadcast address is typically the IPv4 address with the host portion set to either all zeros or all ones.

The proper value for this member is not returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function.

### -field dwReasmSize

Type: <b>DWORD</b>

The maximum re-assembly size for received datagrams.

### -field unused1

Type: <b>unsigned short</b>

This member is reserved.

### -field wType

Type: <b>unsigned short</b>

The address type or state. This member can be a  combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IPADDR_PRIMARY"></a><a id="mib_ipaddr_primary"></a><dl>
<dt><b>MIB_IPADDR_PRIMARY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Primary IP address

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPADDR_DYNAMIC"></a><a id="mib_ipaddr_dynamic"></a><dl>
<dt><b>MIB_IPADDR_DYNAMIC</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Dynamic IP address

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPADDR_DISCONNECTED"></a><a id="mib_ipaddr_disconnected"></a><dl>
<dt><b>MIB_IPADDR_DISCONNECTED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Address is on disconnected interface

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPADDR_DELETED"></a><a id="mib_ipaddr_deleted"></a><dl>
<dt><b>MIB_IPADDR_DELETED</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Address is being deleted

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPADDR_TRANSIENT"></a><a id="mib_ipaddr_transient"></a><dl>
<dt><b>MIB_IPADDR_TRANSIENT</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Transient address

</td>
</tr>
</table>

## -remarks

On Windows XP and later, the <b>dwIndex</b> member of the <b>MIB_IPADDRROW</b> structure has a data type of <b>IF_INDEX</b>. The <b>wType</b> member is only available  on Windows XP and later. On Windows 2000 and earlier, this member is defined as <b>Unused2</b>.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function retrieves the interface–to–IPv4 address mapping table on a local computer and returns this information in an <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a> structure. The <b>table</b> member in the <b>MIB_IPADDRTABLE</b> structure contains an array of <b>MIB_IPADDRROW</b> entries.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IPADDRROW</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## Examples

To view an example that retrieves the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a> structure and then prints out the <b>MIB_IPADDRROW</b> structures in this table, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a>
