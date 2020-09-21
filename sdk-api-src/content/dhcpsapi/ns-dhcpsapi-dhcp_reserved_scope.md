---
UID: NS:dhcpsapi._DHCP_RESERVED_SCOPE
title: DHCP_RESERVED_SCOPE (dhcpsapi.h)
description: The DHCP_RESERVED_SCOPE structure defines a reserved DHCP scope.
helpviewer_keywords: ["*LPDHCP_RESERVED_SCOPE","DHCP_RESERVED_SCOPE","DHCP_RESERVED_SCOPE structure [DHCP]","LPDHCP_RESERVED_SCOPE","LPDHCP_RESERVED_SCOPE structure pointer [DHCP]","dhcp.dhcp_reserved_scope","dhcpsapi/LPDHCP_RESERVED_SCOPE","dhcpsapi/_DHCP_RESERVED_SCOPE"]
old-location: dhcp\dhcp_reserved_scope.htm
tech.root: DHCP
ms.assetid: e3b8bcc1-9cdc-499f-840a-3545ec9b46f7
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_RESERVED_SCOPE, DHCP_RESERVED_SCOPE, DHCP_RESERVED_SCOPE structure [DHCP], LPDHCP_RESERVED_SCOPE, LPDHCP_RESERVED_SCOPE structure pointer [DHCP], dhcp.dhcp_reserved_scope, dhcpsapi/LPDHCP_RESERVED_SCOPE, dhcpsapi/_DHCP_RESERVED_SCOPE'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: DHCP_RESERVED_SCOPE, *LPDHCP_RESERVED_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_RESERVED_SCOPE
 - dhcpsapi/_DHCP_RESERVED_SCOPE
 - LPDHCP_RESERVED_SCOPE
 - dhcpsapi/LPDHCP_RESERVED_SCOPE
 - DHCP_RESERVED_SCOPE
 - dhcpsapi/DHCP_RESERVED_SCOPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_RESERVED_SCOPE
---

# DHCP_RESERVED_SCOPE structure


## -description

The <b>DHCP_RESERVED_SCOPE</b> structure defines a reserved DHCP scope.

## -struct-fields

### -field ReservedIpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains an IP address used to identify the reservation.

### -field ReservedIpSubnetAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet ID of the subnet containing the reservation.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a>