---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP_ARRAY
title: DHCP_FAILOVER_RELATIONSHIP_ARRAY (dhcpsapi.h)
description: The DHCP_FAILOVER_RELATIONSHIP_ARRAY structure defines an array of DHCPv4 failover relationships between partner servers.
helpviewer_keywords: ["*LPDHCP_FAILOVER_RELATIONSHIP_ARRAY","DHCP_FAILOVER_RELATIONSHIP_ARRAY","DHCP_FAILOVER_RELATIONSHIP_ARRAY structure [DHCP]","LPDHCP_FAILOVER_RELATIONSHIP_ARRAY","LPDHCP_FAILOVER_RELATIONSHIP_ARRAY structure pointer [DHCP]","dhcp.dhcp_failover_relationship_array","dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY","dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP_ARRAY"]
old-location: dhcp\dhcp_failover_relationship_array.htm
tech.root: DHCP
ms.assetid: A4C951F9-D5C6-4210-B77D-DBBD6FF2766C
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, LPDHCP_FAILOVER_RELATIONSHIP_ARRAY structure pointer [DHCP], dhcp.dhcp_failover_relationship_array, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP_ARRAY'
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
req.typenames: DHCP_FAILOVER_RELATIONSHIP_ARRAY, *LPDHCP_FAILOVER_RELATIONSHIP_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FAILOVER_RELATIONSHIP_ARRAY
 - dhcpsapi/_DHCP_FAILOVER_RELATIONSHIP_ARRAY
 - LPDHCP_FAILOVER_RELATIONSHIP_ARRAY
 - dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP_ARRAY
 - DHCP_FAILOVER_RELATIONSHIP_ARRAY
 - dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY
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
 - DHCP_FAILOVER_RELATIONSHIP_ARRAY
---

## -description

The <b>DHCP_FAILOVER_RELATIONSHIP_ARRAY</b> structure defines an array of DHCPv4 failover relationships between partner servers.

## -struct-fields

### -field NumElements

Integer that specifies the number of DHCPv4 failover relationships in <b>pRelationships.</b>

### -field pRelationships

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a>  structures.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverenumrelationship">DhcpV4FailoverEnumRelationship</a>
