---
UID: NS:wtsdefs._WTS_SOCKADDR
title: WTS_SOCKADDR (wtsdefs.h)
description: Contains a socket address.
helpviewer_keywords: ["*PWTS_SOCKADDR","PWRDS_SOCKADDR","PWRDS_SOCKADDR structure pointer [Remote Desktop Services]","PWTS_SOCKADDR","PWTS_SOCKADDR structure pointer [Remote Desktop Services]","WRDS_SOCKADDR","WRDS_SOCKADDR structure [Remote Desktop Services]","WTS_SOCKADDR","WTS_SOCKADDR structure [Remote Desktop Services]","termserv.wts_sockaddr","wtsdefs/PWRDS_SOCKADDR","wtsdefs/PWTS_SOCKADDR","wtsdefs/WRDS_SOCKADDR","wtsdefs/WTS_SOCKADDR"]
old-location: termserv\wts_sockaddr.htm
tech.root: TermServ
ms.assetid: 03fb0225-20d1-491a-a052-0a23fa09d01a
ms.date: 12/05/2018
ms.keywords: '*PWTS_SOCKADDR, PWRDS_SOCKADDR, PWRDS_SOCKADDR structure pointer [Remote Desktop Services], PWTS_SOCKADDR, PWTS_SOCKADDR structure pointer [Remote Desktop Services], WRDS_SOCKADDR, WRDS_SOCKADDR structure [Remote Desktop Services], WTS_SOCKADDR, WTS_SOCKADDR structure [Remote Desktop Services], termserv.wts_sockaddr, wtsdefs/PWRDS_SOCKADDR, wtsdefs/PWTS_SOCKADDR, wtsdefs/WRDS_SOCKADDR, wtsdefs/WTS_SOCKADDR'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_SOCKADDR, *PWTS_SOCKADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SOCKADDR
 - wtsdefs/_WTS_SOCKADDR
 - PWTS_SOCKADDR
 - wtsdefs/PWTS_SOCKADDR
 - WTS_SOCKADDR
 - wtsdefs/WTS_SOCKADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_SOCKADDR
---

# WTS_SOCKADDR structure


## -description

Contains a socket address.

## -struct-fields

### -field sin_family

An integer index into the following structure members.

### -field u

### -field u.ipv4

An IPv4 address.

### -field u.ipv4.sin_port

Specifies a TCP or UDP port number.

### -field u.ipv4.in_addr

Specifies the IP address.

### -field u.ipv4.sin_zero

Contains an array of zeros.

### -field u.ipv6

An IPv6 address.

### -field u.ipv6.sin6_port

Specifies a TCP or UDP port number.

### -field u.ipv6.sin6_flowinfo

Contains IPv6 flow information.

### -field u.ipv6.sin6_addr

Specifies the IP address.

### -field u.ipv6.sin6_scope_id

Contains a scope ID

