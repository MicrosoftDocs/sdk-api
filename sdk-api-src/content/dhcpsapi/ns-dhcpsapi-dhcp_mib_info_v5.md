---
UID: NS:dhcpsapi._DHCP_MIB_INFO_V5
title: DHCP_MIB_INFO_V5 (dhcpsapi.h)
description: Contains statistical information about a DHCP server.
helpviewer_keywords: ["*LPDHCP_MIB_INFO_V5","DHCP_MIB_INFO_V5","DHCP_MIB_INFO_V5 structure [DHCP]","LPDHCP_MIB_INFO_V5","LPDHCP_MIB_INFO_V5 structure pointer [DHCP]","dhcp.dhcp_mib_info_v5","dhcpsapi/DHCP_MIB_INFO_V5","dhcpsapi/LPDHCP_MIB_INFO_V5"]
old-location: dhcp\dhcp_mib_info_v5.htm
tech.root: DHCP
ms.assetid: 5081ebce-d3b9-4548-8d80-23d994bce7ab
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_MIB_INFO_V5, DHCP_MIB_INFO_V5, DHCP_MIB_INFO_V5 structure [DHCP], LPDHCP_MIB_INFO_V5, LPDHCP_MIB_INFO_V5 structure pointer [DHCP], dhcp.dhcp_mib_info_v5, dhcpsapi/DHCP_MIB_INFO_V5, dhcpsapi/LPDHCP_MIB_INFO_V5'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: DHCP_MIB_INFO_V5, *LPDHCP_MIB_INFO_V5
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_MIB_INFO_V5
 - dhcpsapi/_DHCP_MIB_INFO_V5
 - LPDHCP_MIB_INFO_V5
 - dhcpsapi/LPDHCP_MIB_INFO_V5
 - DHCP_MIB_INFO_V5
 - dhcpsapi/DHCP_MIB_INFO_V5
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
 - DHCP_MIB_INFO_V5
---

# DHCP_MIB_INFO_V5 structure


## -description

The <b>DHCP_MIB_INFO_V5</b> structure contains statistical information about a DHCP server.

## -struct-fields

### -field Discovers

The number of DISCOVER messages received by the DHCP server.

### -field Offers

The number of OFFER messages sent to DHCP clients.

### -field Requests

The number of REQUEST messages received by  DHCP clients.

### -field Acks

The number of ACK messages sent by the DHCP server.

### -field Naks

The number of NACK messages sent by the DHCP server.

### -field Declines

The number of DECLINE messages sent by DHCP clients.

### -field Releases

The number of RELEASE messages  received by the DHCP server.

### -field ServerStartTime

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the most recent time the DHCP server was started.

### -field QtnNumLeases

This member is not currently used. Please set this to value 0x00000000.

### -field QtnPctQtnLeases

This member is not currently used. Please set this to value 0x00000000.

### -field QtnProbationLeases

This member is not currently used. Please set this to value 0x00000000.

### -field QtnNonQtnLeases

This member is not currently used. Please set this to value 0x00000000.

### -field QtnExemptLeases

This member is not currently used. Please set this to value 0x00000000.

### -field QtnCapableClients

This member is not currently used. Please set this to value 0x00000000.

### -field QtnIASErrors

This member is not currently used. Please set this to value 0x00000000.

### -field DelayedOffers

The number of OFFER messages sent with a specific delay by the DHCP server.

### -field ScopesWithDelayedOffers

The number of scopes with a delay value greater than 0.

### -field Scopes

The total number of scopes configured on the DHCP server

### -field ScopeInfo

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info_v5">SCOPE_MIB_INFO_V5</a> structure that contains specific information about the scopes configured on the DHCP server.

### -field ScopeInfo.size_is

### -field ScopeInfo.size_is.Scopes

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetmibinfov5">DhcpGetMibInfoV5</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info_v5">SCOPE_MIB_INFO_V5</a>