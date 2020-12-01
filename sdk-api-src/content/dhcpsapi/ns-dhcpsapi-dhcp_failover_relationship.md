---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP
title: DHCP_FAILOVER_RELATIONSHIP (dhcpsapi.h)
description: The DHCP_FAILOVER_RELATIONSHIP structure defines information about a DHCPv4 server failover relationship.
helpviewer_keywords: ["*LPDHCP_FAILOVER_RELATIONSHIP","DHCP_FAILOVER_RELATIONSHIP","DHCP_FAILOVER_RELATIONSHIP structure [DHCP]","LPDHCP_FAILOVER_RELATIONSHIP","LPDHCP_FAILOVER_RELATIONSHIP structure pointer [DHCP]","dhcp.dhcp_failover_relationship","dhcpsapi/DHCP_FAILOVER_RELATIONSHIP","dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP"]
old-location: dhcp\dhcp_failover_relationship.htm
tech.root: DHCP
ms.assetid: b409b0ff-2fdc-416c-a7ce-2cba9cf75122
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP, LPDHCP_FAILOVER_RELATIONSHIP structure pointer [DHCP], dhcp.dhcp_failover_relationship, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP'
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
req.typenames: DHCP_FAILOVER_RELATIONSHIP, *LPDHCP_FAILOVER_RELATIONSHIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FAILOVER_RELATIONSHIP
 - dhcpsapi/_DHCP_FAILOVER_RELATIONSHIP
 - LPDHCP_FAILOVER_RELATIONSHIP
 - dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP
 - DHCP_FAILOVER_RELATIONSHIP
 - dhcpsapi/DHCP_FAILOVER_RELATIONSHIP
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
 - DHCP_FAILOVER_RELATIONSHIP
---

## -description

The <b>DHCP_FAILOVER_RELATIONSHIP</b> structure defines information about a DHCPv4 server failover relationship.

## -struct-fields

### -field PrimaryServer

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the primary server IP address.

### -field SecondaryServer

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the secondary server IP address.

### -field Mode

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_failover_mode">DHCP_FAILOVER_MODE</a> enumeration that specifies the failover relationship mode.

### -field ServerType

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_failover_server">DHCP_FAILOVER_SERVER</a> enumeration that specifies if the server is the primary or secondary server in the failover relationship

### -field State

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-fsm_state">FSM_STATE</a> enumeration that specifies the state of the failover relationship.

### -field PrevState

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-fsm_state">FSM_STATE</a> enumeration that specifies the previous state of the failover relationship.

### -field Mclt

A value that specifies the Maximum Client Lead Time (MCLT) in seconds. The MCLT is the maximum time that one server can extend a lease for a client beyond the lease time known by the partner server.

### -field SafePeriod

The time, in seconds, a server will wait before transitioning from the <a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-fsm_state">COMMUNICATION-INT</a> state to a <b>PARTNER-DOWN</b> state. The timer begins when the server enters the <b>COMMUNICATION-INT</b> state.

### -field RelationshipName

Pointer to a null-terminated Unicode string that represents the unique failover relationship name.

### -field PrimaryServerName

Pointer to a null-terminated Unicode string that represents the primary server hostname.

### -field SecondaryServerName

Pointer to a null-terminated Unicode string that represents the secondary server hostname.

### -field pScopes

A pointer to an <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_array">LPDHCP_IP_ARRAY</a> structure that contains the list of IPv4 subnet addresses that are part of the failover relationship and define its scope.

### -field Percentage

Value that specifies the ratio of the client load shared by the primary server in the failover relationship.

### -field SharedSecret

A pointer to a null-terminated Unicode string that represents the shared secret key associated with the failover relationship.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship_array">DHCP_FAILOVER_RELATIONSHIP_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoveraddscopetorelationship">DhcpV4FailoverAddScopeToRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovercreaterelationship">DhcpV4FailoverCreateRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeletescopefromrelationship">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetrelationship">DhcpV4FailoverGetRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscoperelationship">DhcpV4FailoverGetScopeRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoversetrelationship">DhcpV4FailoverSetRelationship</a>