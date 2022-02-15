---
UID: NE:ipmib.__unnamed_enum_4
title: ICMP4_TYPE (ipmib.h)
description: Defines the set of Internet Control Message Protocol (ICMP) for IP version 4.0 (IPv4) message types.
helpviewer_keywords: ["*PICMP4_TYPE","ICMP4_DST_UNREACH","ICMP4_ECHO_REPLY","ICMP4_ECHO_REQUEST","ICMP4_MASK_REPLY","ICMP4_MASK_REQUEST","ICMP4_PARAM_PROB","ICMP4_REDIRECT","ICMP4_ROUTER_ADVERT","ICMP4_ROUTER_SOLICIT","ICMP4_SOURCE_QUENCH","ICMP4_TIMESTAMP_REPLY","ICMP4_TIMESTAMP_REQUEST","ICMP4_TIME_EXCEEDED","ICMP4_TYPE","ICMP4_TYPE enumeration [MIB]","PICMP4_TYPE","PICMP4_TYPE enumeration pointer [MIB]","ipmib/ICMP4_DST_UNREACH","ipmib/ICMP4_ECHO_REPLY","ipmib/ICMP4_ECHO_REQUEST","ipmib/ICMP4_MASK_REPLY","ipmib/ICMP4_MASK_REQUEST","ipmib/ICMP4_PARAM_PROB","ipmib/ICMP4_REDIRECT","ipmib/ICMP4_ROUTER_ADVERT","ipmib/ICMP4_ROUTER_SOLICIT","ipmib/ICMP4_SOURCE_QUENCH","ipmib/ICMP4_TIMESTAMP_REPLY","ipmib/ICMP4_TIMESTAMP_REQUEST","ipmib/ICMP4_TIME_EXCEEDED","ipmib/ICMP4_TYPE","ipmib/PICMP4_TYPE","iprtrmib/ICMP4_DST_UNREACH","iprtrmib/ICMP4_ECHO_REPLY","iprtrmib/ICMP4_ECHO_REQUEST","iprtrmib/ICMP4_MASK_REPLY","iprtrmib/ICMP4_MASK_REQUEST","iprtrmib/ICMP4_PARAM_PROB","iprtrmib/ICMP4_REDIRECT","iprtrmib/ICMP4_ROUTER_ADVERT","iprtrmib/ICMP4_ROUTER_SOLICIT","iprtrmib/ICMP4_SOURCE_QUENCH","iprtrmib/ICMP4_TIMESTAMP_REPLY","iprtrmib/ICMP4_TIMESTAMP_REQUEST","iprtrmib/ICMP4_TIME_EXCEEDED","iprtrmib/ICMP4_TYPE","iprtrmib/PICMP4_TYPE","mib.icmp4_type"]
old-location: mib\icmp4_type.htm
tech.root: MIB
ms.assetid: e284ef78-d3ec-48a4-9d99-d23d84f9456e
ms.date: 12/05/2018
ms.keywords: '*PICMP4_TYPE, ICMP4_DST_UNREACH, ICMP4_ECHO_REPLY, ICMP4_ECHO_REQUEST, ICMP4_MASK_REPLY, ICMP4_MASK_REQUEST, ICMP4_PARAM_PROB, ICMP4_REDIRECT, ICMP4_ROUTER_ADVERT, ICMP4_ROUTER_SOLICIT, ICMP4_SOURCE_QUENCH, ICMP4_TIMESTAMP_REPLY, ICMP4_TIMESTAMP_REQUEST, ICMP4_TIME_EXCEEDED, ICMP4_TYPE, ICMP4_TYPE enumeration [MIB], PICMP4_TYPE, PICMP4_TYPE enumeration pointer [MIB], ipmib/ICMP4_DST_UNREACH, ipmib/ICMP4_ECHO_REPLY, ipmib/ICMP4_ECHO_REQUEST, ipmib/ICMP4_MASK_REPLY, ipmib/ICMP4_MASK_REQUEST, ipmib/ICMP4_PARAM_PROB, ipmib/ICMP4_REDIRECT, ipmib/ICMP4_ROUTER_ADVERT, ipmib/ICMP4_ROUTER_SOLICIT, ipmib/ICMP4_SOURCE_QUENCH, ipmib/ICMP4_TIMESTAMP_REPLY, ipmib/ICMP4_TIMESTAMP_REQUEST, ipmib/ICMP4_TIME_EXCEEDED, ipmib/ICMP4_TYPE, ipmib/PICMP4_TYPE, iprtrmib/ICMP4_DST_UNREACH, iprtrmib/ICMP4_ECHO_REPLY, iprtrmib/ICMP4_ECHO_REQUEST, iprtrmib/ICMP4_MASK_REPLY, iprtrmib/ICMP4_MASK_REQUEST, iprtrmib/ICMP4_PARAM_PROB, iprtrmib/ICMP4_REDIRECT, iprtrmib/ICMP4_ROUTER_ADVERT, iprtrmib/ICMP4_ROUTER_SOLICIT, iprtrmib/ICMP4_SOURCE_QUENCH, iprtrmib/ICMP4_TIMESTAMP_REPLY, iprtrmib/ICMP4_TIMESTAMP_REQUEST, iprtrmib/ICMP4_TIME_EXCEEDED, iprtrmib/ICMP4_TYPE, iprtrmib/PICMP4_TYPE, mib.icmp4_type'
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
req.typenames: ICMP4_TYPE, *PICMP4_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PICMP4_TYPE
 - ipmib/PICMP4_TYPE
 - ICMP4_TYPE
 - ipmib/ICMP4_TYPE
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
 - ICMP4_TYPE
---

# ICMP4_TYPE enumeration


## -description

The <b>ICMP4_TYPE</b> enumeration defines the set of Internet Control Message Protocol (ICMP) for IP version 4.0 (IPv4) message types.

## -enum-fields

### -field ICMP4_ECHO_REPLY:0

ICMP echo reply message.

### -field ICMP4_DST_UNREACH:3

The specified destination for the message is unreachable.

### -field ICMP4_SOURCE_QUENCH:4

ICMP source quench message.

### -field ICMP4_REDIRECT:5

ICMP redirection message.

### -field ICMP4_ECHO_REQUEST:8

ICMP echo redirection message.

### -field ICMP4_ROUTER_ADVERT:9

ICMP router advertisement message.

### -field ICMP4_ROUTER_SOLICIT:10

ICMP router solicitation message.

### -field ICMP4_TIME_EXCEEDED:11

The ICMPv6 message has timed out.

### -field ICMP4_PARAM_PROB:12

The IPv4 header is malformed or contains an incorrect value.

### -field ICMP4_TIMESTAMP_REQUEST:13

ICMP timestamp request message.

### -field ICMP4_TIMESTAMP_REPLY:14

ICMP timestamp reply message.

### -field ICMP4_MASK_REQUEST:17

ICMP mask request message.

### -field ICMP4_MASK_REPLY:18

ICMP mask reply message.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ICMP4_TYPE</b> enumeration  is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

