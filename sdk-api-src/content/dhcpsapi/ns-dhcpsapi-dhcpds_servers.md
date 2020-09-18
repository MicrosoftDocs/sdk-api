---
UID: NS:dhcpsapi._DHCPDS_SERVERS
title: DHCPDS_SERVERS (dhcpsapi.h)
description: The DHCPDS_SERVERS structure defines a list of DHCP servers in the context of directory services.
helpviewer_keywords: ["*LPDHCPDS_SERVERS","*PDHCPDS_SERVERS","DHCPDS_SERVERS","DHCPDS_SERVERS structure [DHCP]","DHCP_SERVER_INFO_ARRAY","DHCP_SERVER_INFO_ARRAY structure [DHCP]","LPDHCPDS_SERVERS *PDHCPDS_SERVERS","LPDHCPDS_SERVERS *PDHCPDS_SERVERS structure pointer [DHCP]","LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY","LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY structure pointer [DHCP]","PDHCPDS_SERVERS","PDHCPDS_SERVERS structure pointer [DHCP]","PDHCP_SERVER_INFO_ARRAY","PDHCP_SERVER_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcpds_servers","dhcpsapi/DHCP_SERVER_INFO_ARRAY","dhcpsapi/LPDHCPDS_SERVERS *PDHCPDS_SERVERS","dhcpsapi/LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY","dhcpsapi/PDHCPDS_SERVERS","dhcpsapi/PDHCP_SERVER_INFO_ARRAY","dhcpsapi/_DHCPDS_SERVERS"]
old-location: dhcp\dhcpds_servers.htm
tech.root: DHCP
ms.assetid: 0f5fe4f3-4eaa-498b-ab48-bfb5ee8f5527
ms.date: 12/05/2018
ms.keywords: '*LPDHCPDS_SERVERS, *PDHCPDS_SERVERS, DHCPDS_SERVERS, DHCPDS_SERVERS structure [DHCP], DHCP_SERVER_INFO_ARRAY, DHCP_SERVER_INFO_ARRAY structure [DHCP], LPDHCPDS_SERVERS *PDHCPDS_SERVERS, LPDHCPDS_SERVERS *PDHCPDS_SERVERS structure pointer [DHCP], LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY, LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY structure pointer [DHCP], PDHCPDS_SERVERS, PDHCPDS_SERVERS structure pointer [DHCP], PDHCP_SERVER_INFO_ARRAY, PDHCP_SERVER_INFO_ARRAY structure pointer [DHCP], dhcp.dhcpds_servers, dhcpsapi/DHCP_SERVER_INFO_ARRAY, dhcpsapi/LPDHCPDS_SERVERS *PDHCPDS_SERVERS, dhcpsapi/LPDHCP_SERVER_INFO_ARRAY *PDHCP_SERVER_INFO_ARRAY, dhcpsapi/PDHCPDS_SERVERS, dhcpsapi/PDHCP_SERVER_INFO_ARRAY, dhcpsapi/_DHCPDS_SERVERS'
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
req.typenames: DHCPDS_SERVERS, *LPDHCPDS_SERVERS, *PDHCPDS_SERVERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPDS_SERVERS
 - dhcpsapi/_DHCPDS_SERVERS
 - LPDHCPDS_SERVERS
 - dhcpsapi/LPDHCPDS_SERVERS
 - DHCPDS_SERVERS
 - dhcpsapi/DHCPDS_SERVERS
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
 - DHCPDS_SERVERS
---

# DHCPDS_SERVERS structure


## -description

The <b>DHCPDS_SERVERS</b> structure defines a list of DHCP servers in the context of directory services.

## -struct-fields

### -field Flags

Reserved. This value should be 0.

### -field NumElements

Specifies the number of elements in <b>Servers</b>.

### -field Servers

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpds_server">DHCPDS_SERVER</a> structures that contain information on individual DHCP servers.