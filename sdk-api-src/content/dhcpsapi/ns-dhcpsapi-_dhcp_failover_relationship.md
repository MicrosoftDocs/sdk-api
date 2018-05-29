---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP
title: "_DHCP_FAILOVER_RELATIONSHIP"
author: windows-sdk-content
description: The DHCP_FAILOVER_RELATIONSHIP structure defines information about a DHCPv4 server failover relationship.
old-location: dhcp\dhcp_failover_relationship.htm
old-project: DHCP
ms.assetid: b409b0ff-2fdc-416c-a7ce-2cba9cf75122
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP, DHCP_FAILOVER_RELATIONSHIP structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP, LPDHCP_FAILOVER_RELATIONSHIP structure pointer [DHCP], _DHCP_FAILOVER_RELATIONSHIP, dhcp.dhcp_failover_relationship, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DHCP_FAILOVER_RELATIONSHIP, *LPDHCP_FAILOVER_RELATIONSHIP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dhcpsapi.h
api_name:
-	DHCP_FAILOVER_RELATIONSHIP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FAILOVER_RELATIONSHIP structure


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

A pointer to an <a href="https://msdn.microsoft.com/84f42e55-8364-4119-83e4-c03699a9aa0a">LPDHCP_IP_ARRAY</a> structure that contains the list of IPv4 subnet addresses that are part of the failover relationship and define its scope.


### -field Percentage

 


### -field SharedSecret

 




#### - mclt

A value that specifies the Maximum Client Lead Time (MCLT) in seconds. The MCLT is the maximum time that one server can extend a lease for a client beyond the lease time known by the partner server.


#### - mode


<a href="https://msdn.microsoft.com/333f70a5-63bd-47f0-bb56-c5f6060e2a72">DHCP_FAILOVER_MODE</a> enumeration that specifies the failover relationship mode.


#### - percentage

Value that specifies the ratio of the client load shared by the primary server in the failover relationship.


#### - prevState


<a href="https://msdn.microsoft.com/a8d0a455-77b3-494c-886e-90136569aada">FSM_STATE</a> enumeration that specifies the previous state of the failover relationship.


#### - primaryServer


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the primary server IP address.


#### - primaryServerName

Pointer to a null-terminated Unicode string that represents the primary server hostname.


#### - relationshipName

Pointer to a null-terminated Unicode string that represents the unique failover relationship name.


#### - safePeriod

The time, in seconds, a server will wait before transitioning from the <a href="https://msdn.microsoft.com/a8d0a455-77b3-494c-886e-90136569aada">COMMUNICATION-INT</a> state to a <b>PARTNER-DOWN</b> state. The timer begins when the server enters the <b>COMMUNICATION-INT</b> state.


#### - secondaryServer


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the secondary server IP address.


#### - secondaryServerName

Pointer to a null-terminated Unicode string that represents the secondary server hostname.


#### - serverType


<a href="https://msdn.microsoft.com/a75a1132-3c49-44f1-a1f6-c98991ebb8c4">DHCP_FAILOVER_SERVER</a> enumeration that specifies if the server is the primary or secondary server in the failover relationship


#### - sharedSecret

A pointer to a null-terminated Unicode string that represents the shared secret key associated with the failover relationship.


#### - state


<a href="https://msdn.microsoft.com/a8d0a455-77b3-494c-886e-90136569aada">FSM_STATE</a> enumeration that specifies the state of the failover relationship.


## -see-also




<a href="https://msdn.microsoft.com/A4C951F9-D5C6-4210-B77D-DBBD6FF2766C">DHCP_FAILOVER_RELATIONSHIP_ARRAY</a>



<a href="https://msdn.microsoft.com/fc54b3dc-86b3-4a18-b05f-7152097f8d5b">DhcpV4FailoverAddScopeToRelationship</a>



<a href="https://msdn.microsoft.com/6e360dd4-b4a0-4652-8754-17c3c284271c">DhcpV4FailoverCreateRelationship</a>



<a href="https://msdn.microsoft.com/52420cc6-0a7b-499b-b7fe-35852a03adea">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="https://msdn.microsoft.com/b637d1e8-8c61-4382-a5ec-3d5395433f86">DhcpV4FailoverGetRelationship</a>



<a href="https://msdn.microsoft.com/795eb9ff-cc44-4567-b496-1bff559290b2">DhcpV4FailoverGetScopeRelationship</a>



<a href="https://msdn.microsoft.com/04012953-dca3-426f-99de-798870d1eb97">DhcpV4FailoverSetRelationship</a>
 

 

