---
UID: NE:ipmib.__unnamed_enum_3
title: ICMP6_TYPE (ipmib.h)
description: Defines the set of Internet Control Message Protocol for IP version 6.0 (ICMPv6) message types.
helpviewer_keywords: ["*PICMP6_TYPE","ICMP6_DST_UNREACH","ICMP6_ECHO_REPLY","ICMP6_ECHO_REQUEST","ICMP6_MEMBERSHIP_QUERY","ICMP6_MEMBERSHIP_REDUCTION","ICMP6_MEMBERSHIP_REPORT","ICMP6_PACKET_TOO_BIG","ICMP6_PARAM_PROB","ICMP6_TIME_EXCEEDED","ICMP6_TYPE","ICMP6_TYPE enumeration [MIB]","ND_NEIGHBOR_ADVERT","ND_NEIGHBOR_SOLICIT","ND_REDIRECT","ND_ROUTER_ADVERT","ND_ROUTER_SOLICIT","PICMP6_TYPE","PICMP6_TYPE enumeration pointer [MIB]","ipmib/ICMP6_DST_UNREACH","ipmib/ICMP6_ECHO_REPLY","ipmib/ICMP6_ECHO_REQUEST","ipmib/ICMP6_MEMBERSHIP_QUERY","ipmib/ICMP6_MEMBERSHIP_REDUCTION","ipmib/ICMP6_MEMBERSHIP_REPORT","ipmib/ICMP6_PACKET_TOO_BIG","ipmib/ICMP6_PARAM_PROB","ipmib/ICMP6_TIME_EXCEEDED","ipmib/ICMP6_TYPE","ipmib/ND_NEIGHBOR_ADVERT","ipmib/ND_NEIGHBOR_SOLICIT","ipmib/ND_REDIRECT","ipmib/ND_ROUTER_ADVERT","ipmib/ND_ROUTER_SOLICIT","ipmib/PICMP6_TYPE","iprtrmib/ICMP6_DST_UNREACH","iprtrmib/ICMP6_ECHO_REPLY","iprtrmib/ICMP6_ECHO_REQUEST","iprtrmib/ICMP6_MEMBERSHIP_QUERY","iprtrmib/ICMP6_MEMBERSHIP_REDUCTION","iprtrmib/ICMP6_MEMBERSHIP_REPORT","iprtrmib/ICMP6_PACKET_TOO_BIG","iprtrmib/ICMP6_PARAM_PROB","iprtrmib/ICMP6_TIME_EXCEEDED","iprtrmib/ICMP6_TYPE","iprtrmib/ND_NEIGHBOR_ADVERT","iprtrmib/ND_NEIGHBOR_SOLICIT","iprtrmib/ND_REDIRECT","iprtrmib/ND_ROUTER_ADVERT","iprtrmib/ND_ROUTER_SOLICIT","iprtrmib/PICMP6_TYPE","mib.icmp6_type"]
old-location: mib\icmp6_type.htm
tech.root: MIB
ms.assetid: d20f72a3-4e9e-43ea-b7b1-c21940c219fc
ms.date: 12/05/2018
ms.keywords: '*PICMP6_TYPE, ICMP6_DST_UNREACH, ICMP6_ECHO_REPLY, ICMP6_ECHO_REQUEST, ICMP6_MEMBERSHIP_QUERY, ICMP6_MEMBERSHIP_REDUCTION, ICMP6_MEMBERSHIP_REPORT, ICMP6_PACKET_TOO_BIG, ICMP6_PARAM_PROB, ICMP6_TIME_EXCEEDED, ICMP6_TYPE, ICMP6_TYPE enumeration [MIB], ND_NEIGHBOR_ADVERT, ND_NEIGHBOR_SOLICIT, ND_REDIRECT, ND_ROUTER_ADVERT, ND_ROUTER_SOLICIT, PICMP6_TYPE, PICMP6_TYPE enumeration pointer [MIB], ipmib/ICMP6_DST_UNREACH, ipmib/ICMP6_ECHO_REPLY, ipmib/ICMP6_ECHO_REQUEST, ipmib/ICMP6_MEMBERSHIP_QUERY, ipmib/ICMP6_MEMBERSHIP_REDUCTION, ipmib/ICMP6_MEMBERSHIP_REPORT, ipmib/ICMP6_PACKET_TOO_BIG, ipmib/ICMP6_PARAM_PROB, ipmib/ICMP6_TIME_EXCEEDED, ipmib/ICMP6_TYPE, ipmib/ND_NEIGHBOR_ADVERT, ipmib/ND_NEIGHBOR_SOLICIT, ipmib/ND_REDIRECT, ipmib/ND_ROUTER_ADVERT, ipmib/ND_ROUTER_SOLICIT, ipmib/PICMP6_TYPE, iprtrmib/ICMP6_DST_UNREACH, iprtrmib/ICMP6_ECHO_REPLY, iprtrmib/ICMP6_ECHO_REQUEST, iprtrmib/ICMP6_MEMBERSHIP_QUERY, iprtrmib/ICMP6_MEMBERSHIP_REDUCTION, iprtrmib/ICMP6_MEMBERSHIP_REPORT, iprtrmib/ICMP6_PACKET_TOO_BIG, iprtrmib/ICMP6_PARAM_PROB, iprtrmib/ICMP6_TIME_EXCEEDED, iprtrmib/ICMP6_TYPE, iprtrmib/ND_NEIGHBOR_ADVERT, iprtrmib/ND_NEIGHBOR_SOLICIT, iprtrmib/ND_REDIRECT, iprtrmib/ND_ROUTER_ADVERT, iprtrmib/ND_ROUTER_SOLICIT, iprtrmib/PICMP6_TYPE, mib.icmp6_type'
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: ICMP6_TYPE, *PICMP6_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PICMP6_TYPE
 - ipmib/PICMP6_TYPE
 - ICMP6_TYPE
 - ipmib/ICMP6_TYPE
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
 - ICMP6_TYPE
---

# ICMP6_TYPE enumeration


## -description

The <b>ICMP6_TYPE</b> enumeration defines the set of Internet Control Message Protocol for IP version 6.0 (ICMPv6)  message types.

## -enum-fields

### -field ICMP6_DST_UNREACH:1

The specified destination for the message is unreachable.

### -field ICMP6_PACKET_TOO_BIG:2

The ICMPv6 packet is too large.

### -field ICMP6_TIME_EXCEEDED:3

The ICMPv6 message has timed out.

### -field ICMP6_PARAM_PROB:4

The IPv6 header is malformed or contains an incorrect value.

### -field ICMP6_ECHO_REQUEST:128

ICMPv6 echo request message.

### -field ICMP6_ECHO_REPLY:129

ICMPv6 echo reply message.

### -field ICMP6_MEMBERSHIP_QUERY:130

ICMPv6 group membership query message.

### -field ICMP6_MEMBERSHIP_REPORT:131

ICMPv6 group membership report message.

### -field ICMP6_MEMBERSHIP_REDUCTION:132

ICMPv6 group membership reduction message.

### -field ND_ROUTER_SOLICIT:133

ICMPv6 router solicitation message.

### -field ND_ROUTER_ADVERT:134

ICMPv6 router advertisement message.

### -field ND_NEIGHBOR_SOLICIT:135

ICMPv6 network neighbor solicitation message.

### -field ND_NEIGHBOR_ADVERT:136

ICMPv6 network neighbor advertisement message.

### -field ND_REDIRECT:137

ICMPv6 packet redirection message.

### -field ICMP6_V2_MEMBERSHIP_REPORT:143

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ICMP6_TYPE</b> enumeration  is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

