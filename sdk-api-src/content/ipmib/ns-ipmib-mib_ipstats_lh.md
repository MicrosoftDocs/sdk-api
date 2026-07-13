---
UID: NS:ipmib._MIB_IPSTATS_LH
title: MIB_IPSTATS_LH (ipmib.h)
description: MIB_IPSTATS_LH (ipmib.h) stores information about the IP protocol running on a particular computer.
helpviewer_keywords: ["*PMIB_IPSTATS","*PMIB_IPSTATS_LH","MIB_IPSTATS","MIB_IPSTATS structure [MIB]","MIB_IPSTATS_LH","MIB_IP_FORWARDING","MIB_IP_NOT_FORWARDING","MIB_USE_CURRENT_FORWARDING","PMIB_IPSTATS","PMIB_IPSTATS structure pointer [MIB]","_mpr_mib_ipstats","ipmib/MIB_IPSTATS","ipmib/PMIB_IPSTATS","iprtrmib/MIB_IPSTATS","iprtrmib/PMIB_IPSTATS","mib.mib_ipstats","rras.mib_ipstats"]
old-location: mib\mib_ipstats.htm
tech.root: MIB
ms.assetid: 920e71b6-247c-4442-9f66-704a6c878feb
ms.date: 08/03/2022
ms.keywords: '*PMIB_IPSTATS, *PMIB_IPSTATS_LH, MIB_IPSTATS, MIB_IPSTATS structure [MIB], MIB_IPSTATS_LH, MIB_IP_FORWARDING, MIB_IP_NOT_FORWARDING, MIB_USE_CURRENT_FORWARDING, PMIB_IPSTATS, PMIB_IPSTATS structure pointer [MIB], _mpr_mib_ipstats, ipmib/MIB_IPSTATS, ipmib/PMIB_IPSTATS, iprtrmib/MIB_IPSTATS, iprtrmib/PMIB_IPSTATS, mib.mib_ipstats, rras.mib_ipstats'
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
req.typenames: MIB_IPSTATS_LH, *PMIB_IPSTATS_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPSTATS_LH
 - ipmib/_MIB_IPSTATS_LH
 - PMIB_IPSTATS_LH
 - ipmib/PMIB_IPSTATS_LH
 - MIB_IPSTATS_LH
 - ipmib/MIB_IPSTATS_LH
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
 - MIB_IPSTATS
---

# MIB_IPSTATS_LH structure


## -description

The 
<b>MIB_IPSTATS</b> structure stores information about the IP protocol running on a particular computer.

## -struct-fields

### -field dwForwarding

Type: <b>DWORD</b>

Specifies whether IP forwarding is enabled or disabled for a protocol (IPv4 or IPv6).

On Windows Vista and later, this member is defined as a union containing a <b>DWORD dwForwarding</b> member and a <b>MIB_IPSTATS_FORWARDING Forwarding</b> member where <b>MIB_IPSTATS_FORWARDING</b> is an enumeration defined in the <i>Ipmib.h</i> header file.

<div class="alert"><b>Note</b>   This member applies to the entire system per protocol (IPv4 or IPv6) and doesn’t return per interface configuration for IP forwarding.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IP_FORWARDING"></a><a id="mib_ip_forwarding"></a><dl>
<dt><b>MIB_IP_FORWARDING</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
IP forwarding is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IP_NOT_FORWARDING"></a><a id="mib_ip_not_forwarding"></a><dl>
<dt><b>MIB_IP_NOT_FORWARDING</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
IP forwarding is not enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_USE_CURRENT_FORWARDING"></a><a id="mib_use_current_forwarding"></a><dl>
<dt><b>MIB_USE_CURRENT_FORWARDING</b></dt>
<dt>0xffff</dt>
</dl>
</td>
<td width="60%">
Use the current IP forwarding setting. This value is only applicable when setting the forwarding and time-to-live (TTL) options using the <b>SetIpStatistics</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatisticsex">SetIpStatisticsEx</a> functions.

</td>
</tr>
</table>

### -field Forwarding

### -field dwDefaultTTL

Type: <b>DWORD</b>

The default initial time-to-live (TTL) for datagrams originating on a particular computer.

This member can be set to <b>MIB_USE_CURRENT_TTL</b> to use the current default TTL value when setting the forwarding and time-to-live (TTL) options using the <b>SetIpStatistics</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatisticsex">SetIpStatisticsEx</a> functions.

### -field dwInReceives

Type: <b>DWORD</b>

The number of datagrams received.

### -field dwInHdrErrors

Type: <b>DWORD</b>

The number of datagrams received that have header errors.

### -field dwInAddrErrors

Type: <b>DWORD</b>

The number of datagrams received that have address errors.

### -field dwForwDatagrams

Type: <b>DWORD</b>

The number of datagrams forwarded.

### -field dwInUnknownProtos

Type: <b>DWORD</b>

The number of datagrams received that have an unknown protocol.

### -field dwInDiscards

Type: <b>DWORD</b>

The number of received datagrams discarded.

### -field dwInDelivers

Type: <b>DWORD</b>

The number of received datagrams delivered.

### -field dwOutRequests

Type: <b>DWORD</b>

The number of outgoing datagrams that IP is requested to transmit. This number does not include forwarded datagrams.

### -field dwRoutingDiscards

Type: <b>DWORD</b>

The number of outgoing datagrams discarded.

### -field dwOutDiscards

Type: <b>DWORD</b>

The number of transmitted datagrams discarded.

### -field dwOutNoRoutes

Type: <b>DWORD</b>

The number of datagrams for which this computer did not have a route to the destination IP address. These datagrams were discarded.

### -field dwReasmTimeout

Type: <b>DWORD</b>

The amount of time allowed for all pieces of a fragmented datagram to arrive. If all pieces do not arrive within this time, the datagram is discarded.

### -field dwReasmReqds

Type: <b>DWORD</b>

The number of datagrams that require re-assembly.

### -field dwReasmOks

Type: <b>DWORD</b>

The number of datagrams that were successfully reassembled.

### -field dwReasmFails

Type: <b>DWORD</b>

The number of datagrams that cannot be reassembled.

### -field dwFragOks

Type: <b>DWORD</b>

The number of datagrams that were fragmented successfully.

### -field dwFragFails

Type: <b>DWORD</b>

The number of datagrams that have not been fragmented because the IP header specifies no fragmentation. These datagrams are discarded.

### -field dwFragCreates

Type: <b>DWORD</b>

The number of fragments created.

### -field dwNumIf

Type: <b>DWORD</b>

The number of interfaces.

### -field dwNumAddr

Type: <b>DWORD</b>

The number of IP addresses associated with this computer.

### -field dwNumRoutes

Type: <b>DWORD</b>

The number of routes in the IP routing table.

## -remarks

The 
<b>MIB_IPSTATS</b> structure stores information per protocol (IPv4 or IPv6).

The <b>dwForwarding</b> member specifies the per-protocol forwarding state for IPv4 or IPv6, not  the forwarding state for an interface. The forwarding state of each interface state is the state that is in affect for that interface. The per-protocol state returned by the <b>GetIpStatistics</b> or the <b>GetIpStatisticsEx</b> function is not the forwarding state in affect. The <b>dwForwarding</b> member exists to serve two purposes:

<ul>
<li>Provides a default value for the forwarding state when a new interface is created with no specific forwarding state (neither disabled nor enabled) . This value is inherited per-protocol state.</li>
<li>Provides a value set by a domain administrator to enable or disable a per-protocol forwarding state. The forwarding states of all interfaces using that protocol are also enabled or disabled.
</li>
</ul>
On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IPSTATS</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<b>GetIpStatistics</b>



<b>GetIpStatisticsEx</b>



<b>SetIpStatistics</b>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatisticsex">SetIpStatisticsEx</a>
