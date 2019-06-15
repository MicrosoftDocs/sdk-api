---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP
title: DHCP_FAILOVER_RELATIONSHIP (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_FAILOVER_RELATIONSHIP structure defines information about a DHCPv4 server failover relationship.
old-location: dhcp\dhcp_failover_relationship.htm
tech.root: DHCP
ms.assetid: b409b0ff-2fdc-416c-a7ce-2cba9cf75122
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP, LPDHCP_FAILOVER_RELATIONSHIP structure pointer [DHCP], dhcp.dhcp_failover_relationship, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_FAILOVER_RELATIONSHIP
product: Windows
targetos: Windows
req.typenames: DHCP_FAILOVER_RELATIONSHIP, *LPDHCP_FAILOVER_RELATIONSHIP
req.redist: 
ms.custom: 19H1
---

# DHCP_FAILOVER_RELATIONSHIP structure


## -description


The <b>DHCP_FAILOVER_RELATIONSHIP</b> structure defines information about a DHCPv4 server failover relationship.


## -struct-fields




### -field PrimaryServer

 


### -field SecondaryServer

 


### -field Mode

 


### -field ServerType

 


### -field State

 


### -field PrevState

 


### -field Mclt

 


### -field SafePeriod

 


### -field RelationshipName

 


### -field PrimaryServerName

 


### -field SecondaryServerName

 


### -field pScopes

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_array">LPDHCP_IP_ARRAY</a> structure that contains the list of IPv4 subnet addresses that are part of the failover relationship and define its scope.


### -field Percentage

 


### -field SharedSecret

 




#### - mclt

A value that specifies the Maximum Client Lead Time (MCLT) in seconds. The MCLT is the maximum time that one server can extend a lease for a client beyond the lease time known by the partner server.


#### - mode


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_dhcp_failover_mode">DHCP_FAILOVER_MODE</a> enumeration that specifies the failover relationship mode.


#### - percentage

Value that specifies the ratio of the client load shared by the primary server in the failover relationship.


#### - prevState


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_fsm_state">FSM_STATE</a> enumeration that specifies the previous state of the failover relationship.


#### - primaryServer


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the primary server IP address.


#### - primaryServerName

Pointer to a null-terminated Unicode string that represents the primary server hostname.


#### - relationshipName

Pointer to a null-terminated Unicode string that represents the unique failover relationship name.


#### - safePeriod

The time, in seconds, a server will wait before transitioning from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_fsm_state">COMMUNICATION-INT</a> state to a <b>PARTNER-DOWN</b> state. The timer begins when the server enters the <b>COMMUNICATION-INT</b> state.


#### - secondaryServer


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the secondary server IP address.


#### - secondaryServerName

Pointer to a null-terminated Unicode string that represents the secondary server hostname.


#### - serverType


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_dhcp_failover_server">DHCP_FAILOVER_SERVER</a> enumeration that specifies if the server is the primary or secondary server in the failover relationship


#### - sharedSecret

A pointer to a null-terminated Unicode string that represents the shared secret key associated with the failover relationship.


#### - state


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_fsm_state">FSM_STATE</a> enumeration that specifies the state of the failover relationship.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_failover_relationship_array">DHCP_FAILOVER_RELATIONSHIP_ARRAY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoveraddscopetorelationship">DhcpV4FailoverAddScopeToRelationship</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovercreaterelationship">DhcpV4FailoverCreateRelationship</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeletescopefromrelationship">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetrelationship">DhcpV4FailoverGetRelationship</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscoperelationship">DhcpV4FailoverGetScopeRelationship</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoversetrelationship">DhcpV4FailoverSetRelationship</a>
 

 

