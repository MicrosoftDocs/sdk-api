---
UID: NS:tcpioctl.IPAddrEntry
title: IPAddrEntry (tcpioctl.h)
description: Implements part of the Management Information Base (MIB-II) information group for the Internet Protocol (IP) as specified in the Internet Engineering Task Force (IETF) Request for Comments (RFC) 2011. (IPAddrEntry)
helpviewer_keywords: ["IPAddrEntry","IPAddrEntry structure [Windows API]","tcpioctl/IPAddrEntry","winprog.ipaddrentry"]
old-location: winprog\ipaddrentry.htm
tech.root: winprog
ms.assetid: c48453e8-05f1-49d8-bae6-fad0681bdf7e
ms.date: 12/05/2018
ms.keywords: IPAddrEntry, IPAddrEntry structure [Windows API], tcpioctl/IPAddrEntry, winprog.ipaddrentry
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
req.typenames: IPAddrEntry
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPAddrEntry
 - tcpioctl/IPAddrEntry
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
 - IPAddrEntry
---

# IPAddrEntry structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Implements part of the Management Information Base (MIB-II) 
			information group for the Internet Protocol (IP) as specified in the 
			Internet Engineering Task Force (IETF) Request for Comments <a href="https://www.ietf.org/rfc/rfc2011.txt">(RFC) 2011</a>.

## -struct-fields

### -field iae_addr

An IPv4 IP address to which this structure pertains.

### -field iae_index

The index value that uniquely identifies the interface associated with this
					IP address.

### -field iae_mask

The subnet mask associated with this IP address. The value of the mask is an 
					IPv4 address with all the network bits set to 1 and all the hosts bits set to 0.

### -field iae_bcastaddr

The value of the least-significant bit in the IP broadcast address used for 
					sending datagrams on the logical interface associated with this IP address. 
					For example, when the Internet standard all-ones broadcast address 
					is used, the value is 1. This value applies to both the subnet and network 
					broadcast addresses used by the entity on this logical interface.

### -field iae_reasmsize

The size of the largest IP datagram that this entity can reassemble from 
					incoming IP fragmented datagrams received on this interface.

### -field iae_context

A context value for this IP address.

### -field iae_pad

A pad value.

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">Management Information Base
			 Reference</a>
