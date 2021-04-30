---
UID: NS:ws2ipdef.icmp_error_info
title: ICMP_ERROR_INFO
author: windows-sdk-content
description: Used to store received ICMP error information.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/04/2019
ms.keywords: "*PICMP_ERROR_INFO, ICMP_ERROR_INFO [Winsock], ICMP_ERROR_INFO, ICMP_ERROR_INFO structure [Winsock], PICMP_ERROR_INFO, PICMP_ERROR_INFO structure pointer [Winsock], icmp_error_info, icmp_error_info structure [Winsock], ws2ipdef.icmp_error_info, ws2ipdef/PICMP_ERROR_INFO, ws2ipdef/icmp_error_info, ws2ipdef/PICMP_ERROR_INFO, ws2ipdef/icmp_error_info"
req.header: ws2ipdef.h
req.include-header: ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
req.typenames: ICMP_ERROR_INFO, *PICMP_ERROR_INFO
req.redist: 
f1_keywords:
 - icmp_error_info
 - ws2ipdef/icmp_error_info
 - PICMP_ERROR_INFO
 - ws2ipdef/PICMP_ERROR_INFO
 - ICMP_ERROR_INFO
 - ws2ipdef/ICMP_ERROR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2ipdef.h
 - ws2tcpip.h
api_name:
 - ICMP_ERROR_INFO
---

## -description

Used to store received ICMP error information.

## -struct-fields

### -field srcaddress

Type: **[SOCKADDR_INET](./ns-ws2ipdef-sockaddr_inet.md)**

The source IP address of the ICMP error.

### -field protocol

Type: **IPPROTO**

The protocol of the ICMP error (either **IPPROTO_ICMP** or **IPPROTO_ICMPV6**).

### -field type

Type: **[UINT8](/windows/win32/winprog/windows-data-types)**

The ICMP error type.

### -field code

Type: **[UINT8](/windows/win32/winprog/windows-data-types)**

The ICMP error code.

## -remarks

## -see-also