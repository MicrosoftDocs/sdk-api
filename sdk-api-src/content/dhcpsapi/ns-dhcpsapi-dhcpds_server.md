---
UID: NS:dhcpsapi._DHCPDS_SERVER
title: DHCPDS_SERVER (dhcpsapi.h)
description: The DHCPDS_SERVER structure defines information on a DHCP server in the context of directory services.
helpviewer_keywords: ["*LPDHCPDS_SERVER","*PDHCPDS_SERVER","DHCPDS_SERVER","DHCPDS_SERVER structure [DHCP]","DHCP_SERVER_INFO","DHCP_SERVER_INFO structure [DHCP]","LPDHCPDS_SERVER *PDHCPDS_SERVER","LPDHCPDS_SERVER *PDHCPDS_SERVER structure pointer [DHCP]","LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO","LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO structure pointer [DHCP]","PDHCPDS_SERVER","PDHCPDS_SERVER structure pointer [DHCP]","PDHCP_SERVER_INFO","PDHCP_SERVER_INFO structure pointer [DHCP]","dhcp.dhcpds_server","dhcpsapi/DHCP_SERVER_INFO","dhcpsapi/LPDHCPDS_SERVER *PDHCPDS_SERVER","dhcpsapi/LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO","dhcpsapi/PDHCPDS_SERVER","dhcpsapi/PDHCP_SERVER_INFO","dhcpsapi/_DHCPDS_SERVER"]
old-location: dhcp\dhcpds_server.htm
tech.root: DHCP
ms.assetid: 12f3fbd3-9b81-4a11-914c-83658c2bce89
ms.date: 12/05/2018
ms.keywords: '*LPDHCPDS_SERVER, *PDHCPDS_SERVER, DHCPDS_SERVER, DHCPDS_SERVER structure [DHCP], DHCP_SERVER_INFO, DHCP_SERVER_INFO structure [DHCP], LPDHCPDS_SERVER *PDHCPDS_SERVER, LPDHCPDS_SERVER *PDHCPDS_SERVER structure pointer [DHCP], LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO, LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO structure pointer [DHCP], PDHCPDS_SERVER, PDHCPDS_SERVER structure pointer [DHCP], PDHCP_SERVER_INFO, PDHCP_SERVER_INFO structure pointer [DHCP], dhcp.dhcpds_server, dhcpsapi/DHCP_SERVER_INFO, dhcpsapi/LPDHCPDS_SERVER *PDHCPDS_SERVER, dhcpsapi/LPDHCP_SERVER_INFO *PDHCP_SERVER_INFO, dhcpsapi/PDHCPDS_SERVER, dhcpsapi/PDHCP_SERVER_INFO, dhcpsapi/_DHCPDS_SERVER'
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
req.typenames: DHCPDS_SERVER, *LPDHCPDS_SERVER, *PDHCPDS_SERVER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPDS_SERVER
 - dhcpsapi/_DHCPDS_SERVER
 - LPDHCPDS_SERVER
 - dhcpsapi/LPDHCPDS_SERVER
 - DHCPDS_SERVER
 - dhcpsapi/DHCPDS_SERVER
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
 - DHCPDS_SERVER
---

# DHCPDS_SERVER structure


## -description

The <b>DHCPDS_SERVER</b> structure defines information on a DHCP server in the context of directory services.

## -struct-fields

### -field Version

Reserved. This value should be set to 0.

### -field ServerName

Unicode string that contains the unique name of the DHCP server.

### -field ServerAddress

Specifies the IP address of the DHCP server as an unsigned 32-bit integer.

### -field Flags

Specifies a set of bit flags that describe active directory settings for the DHCP server.

### -field State

Reserved. This value should be set to 0.

### -field DsLocation

Unicode string that contains the active directory path to the DHCP server.

### -field DsLocType

Reserved. This value should be set to 0.

