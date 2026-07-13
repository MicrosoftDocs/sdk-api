---
UID: NS:tcpioctl.IPSNMPInfo
title: IPSNMPInfo (tcpioctl.h)
description: Implements part of the Management Information Base (MIB-II) information group for the Internet Protocol (IP) as specified in the Internet Engineering Task Force (IETF) Request for Comments (RFC) 2011. (IPSNMPInfo)
helpviewer_keywords: ["IPSNMPInfo","IPSNMPInfo structure [Windows API]","tcpioctl/IPSNMPInfo","winprog.ipsnmpinfo"]
old-location: winprog\ipsnmpinfo.htm
tech.root: winprog
ms.assetid: eb25fae9-1a89-4474-bcb6-28c09bc3e0c9
ms.date: 12/05/2018
ms.keywords: IPSNMPInfo, IPSNMPInfo structure [Windows API], tcpioctl/IPSNMPInfo, winprog.ipsnmpinfo
req.header: tcpioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IPSNMPInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSNMPInfo
 - tcpioctl/IPSNMPInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpioctl.h
api_name:
 - IPSNMPInfo
---

# IPSNMPInfo structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Implements part of the Management Information Base (MIB-II) 
			information group for the Internet Protocol (IP) as specified in the 
			Internet Engineering Task Force (IETF) Request for Comments <a href="https://www.ietf.org/rfc/rfc2011.txt">(RFC) 2011</a>.

## -struct-fields

### -field ipsi_forwarding

Indicates whether this entity is acting as an IP router that forwards datagrams 
					not addressed to it. IP routers forward datagrams but IP hosts do not, except for datagrams 
					source-routed through the host.

### -field ipsi_defaultttl

The default value for the Time-To-Live (TTL) field of the IP header of datagrams 
					that originate at this entity, inserted whenever the transport layer protocol 
					does not supply a TTL value.

### -field ipsi_inreceives

The total number of input datagrams received from interfaces by this 
					entity, including those received in error.

### -field ipsi_inhdrerrors

The number of input datagrams discarded because of errors in their IP headers. Such errors include bad 
					checksums, version-number mismatch, other format errors, time-to-live 
					exceeded and errors discovered in processing the IP options, but not including invalid destination addresses.

### -field ipsi_inaddrerrors

The number of input datagrams discarded because the IP address in the 
					destination field of their IP header was not valid for this entity. This includes 
					invalid addresses such as 0.0.0.0, addresses of unsupported Classes 
					such as Class E, and, for entities that are not IP router datagrams, includes 
					all addresses that are not local.

### -field ipsi_forwdatagrams

The number of input datagrams for which this entity was not their final IP 
					destination, so that an attempt was made to forward them. In entities that do 
					not act as IP routers, this counter  includes only those packets that are 
					successfully source-routed through this entity.

### -field ipsi_inunknownprotos

The number of locally-addressed datagrams received successfully but discarded 
					because of an unknown or unsupported protocol.

### -field ipsi_indiscards

The number of input IP datagrams that contained nothing to prevent their 
					continued processing, but  were discarded for run-time reasons, such as lack 
					of available memory or other resources. Note that this counter does not include 
					any datagrams discarded while awaiting reassembly.

### -field ipsi_indelivers

The total number of input datagrams successfully delivered to IP user protocols, 
					including ICMP.

### -field ipsi_outrequests

The total number of IP datagrams that local IP user protocols, including ICMP, 
					supplied to IP in requests for transmission. Note that this counter does not 
					include any datagrams counted in the <b>ipsi_forwdatagrams</b> member.

### -field ipsi_routingdiscards

The number of valid routing entries that were discarded for reasons such as the need
					to free up memory.

### -field ipsi_outdiscards

The number of output IP datagrams for which no problem was encountered to 
					prevent their transmission, but that were discarded for run-time reasons such as 
					lack of memory or other resources.  Note that this counter includes datagrams 
					also counted in the <b>ipsi_forwdatagrams</b> member if any 
					such packets were discarded in this way.

### -field ipsi_outnoroutes

The number of IP datagrams discarded because no route could be found to transmit 
					them to their destination. This value includes packets also counted in the 
					<b>ipsi_forwdatagrams</b> member that cannot be routed, and 
					datagrams that a host cannot route because its default routers are all down.

### -field ipsi_reasmtimeout

The maximum number of seconds that this entity holds received fragments that are 
					awaiting reassembly before discarding them.

### -field ipsi_reasmreqds

The number of IP fragments received at this entity that needed to be reassembled.

### -field ipsi_reasmoks

The number of IP datagrams that have been successfully reassembled at this entity.

### -field ipsi_reasmfails

The number of reassembly failures of any sort detected by the IP reassembly 
					algorithm. Note that this is not necessarily a count of discarded IP fragments, 
					because some algorithms such as that described in <a href="https://www.ietf.org/rfc/rfc815.txt">RFC 815</a> do not keep track of 
					the number of fragments being combined.

### -field ipsi_fragoks

The number of IP datagrams that have been successfully fragmented at this entity.

### -field ipsi_fragfails

The number of IP datagrams that have been discarded because they needed to be 
					fragmented at this entity but could not be, because their "Don't Fragment" 
					flag was set or for some other reason.

### -field ipsi_fragcreates

The number of IP datagram fragments that have been generated as a result of 
					fragmentation at this entity.

### -field ipsi_numif

The number of interfaces on which this entity listens.

### -field ipsi_numaddr

The number of IP addresses for which this entity listens.

### -field ipsi_numroutes

The number of routes in this entity's route table.

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">Management Information Base
			 Reference</a>
