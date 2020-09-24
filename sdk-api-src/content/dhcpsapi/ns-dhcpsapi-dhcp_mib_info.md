---
UID: NS:dhcpsapi._DHCP_MIB_INFO
title: DHCP_MIB_INFO (dhcpsapi.h)
description: Defines information returned from the DHCP-specific SNMP Management Information Block (MIB) about the current DHCP service.
helpviewer_keywords: ["*LPDHCP_MIB_INFO","DHCP_MIB_INFO","DHCP_MIB_INFO structure [DHCP]","LPDHCP_MIB_INFO","LPDHCP_MIB_INFO structure pointer [DHCP]","dhcp.dhcp_mib_info","dhcpsapi/LPDHCP_MIB_INFO","dhcpsapi/_DHCP_MIB_INFO"]
old-location: dhcp\dhcp_mib_info.htm
tech.root: DHCP
ms.assetid: 58f3e3a3-8246-48ff-be45-20a7eed1ed0e
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_MIB_INFO, DHCP_MIB_INFO, DHCP_MIB_INFO structure [DHCP], LPDHCP_MIB_INFO, LPDHCP_MIB_INFO structure pointer [DHCP], dhcp.dhcp_mib_info, dhcpsapi/LPDHCP_MIB_INFO, dhcpsapi/_DHCP_MIB_INFO'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_MIB_INFO, *LPDHCP_MIB_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_MIB_INFO
 - dhcpsapi/_DHCP_MIB_INFO
 - LPDHCP_MIB_INFO
 - dhcpsapi/LPDHCP_MIB_INFO
 - DHCP_MIB_INFO
 - dhcpsapi/DHCP_MIB_INFO
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
 - DHCP_MIB_INFO
---

# DHCP_MIB_INFO structure


## -description

The <b>DHCP_MIB_INFO</b> structure defines information returned from the DHCP-specific SNMP Management Information Block (MIB) about the current DHCP service.

## -struct-fields

### -field Discovers

Contains the number of DHCP discovery messages received.

### -field Offers

Contains the number of DHCP service offer messages transmitted.

### -field Requests

Contains the number of dynamic address request messages received.

### -field Acks

Contains the number of DHCP ACK messages received.

### -field Naks

Contains the number of DHCP NACK messages received.

### -field Declines

Contains the number of dynamic address service decline messages received.

### -field Releases

Contains the number of dynamic address release messages received.

### -field ServerStartTime

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the date and time the DHCP service started.

### -field Scopes

Contains the number of scopes defined on the DHCP server.

### -field ScopeInfo

Array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info">SCOPE_MIB_INFO</a> structures that contain information on each subnet defined on the server. There are exactly <b>Scopes</b> elements in this array. If no subnets are defined (<b>Scopes</b> is 0), this field will be <b>NULL</b>.

### -field ScopeInfo.size_is

### -field ScopeInfo.size_is.Scopes

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info">SCOPE_MIB_INFO</a>