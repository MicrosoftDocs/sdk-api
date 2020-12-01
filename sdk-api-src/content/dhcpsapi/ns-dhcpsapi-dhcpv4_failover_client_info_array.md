---
UID: NS:dhcpsapi._DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
title: DHCPV4_FAILOVER_CLIENT_INFO_ARRAY (dhcpsapi.h)
description: The DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure defines an array of DHCP server scope statistics that are part of a failover relationship.
helpviewer_keywords: ["*LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY","DHCPV4_FAILOVER_CLIENT_INFO_ARRAY","DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure [DHCP]","PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY","PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcpv4_failover_client_info_array","dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO_ARRAY","dhcpsapi/PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY"]
old-location: dhcp\dhcpv4_failover_client_info_array.htm
tech.root: DHCP
ms.assetid: D988F420-28F0-4F13-B2A1-CFD9A71669A4
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY, DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure [DHCP], PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY, PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure pointer [DHCP], dhcp.dhcpv4_failover_client_info_array, dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, dhcpsapi/PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, *LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
 - dhcpsapi/_DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
 - LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY
 - dhcpsapi/LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY
 - DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
 - dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
---

# DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure


## -description

The <b>DHCPV4_FAILOVER_CLIENT_INFO_ARRAY</b> structure defines an array of DHCP server scope statistics that are part of a failover relationship.

## -struct-fields

### -field NumElements

Integer that specifies the number of DHCP server scope statistics in <b>Clients</b>.

### -field Clients

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv4_failover_client_info">DHCPV4_FAILOVER_CLIENT_INFO</a>  structures.

### -field Clients.size_is

### -field Clients.size_is.NumElements