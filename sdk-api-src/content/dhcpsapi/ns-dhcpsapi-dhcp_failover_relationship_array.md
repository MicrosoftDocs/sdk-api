---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP_ARRAY
title: DHCP_FAILOVER_RELATIONSHIP_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_FAILOVER_RELATIONSHIP_ARRAY structure defines an array of DHCPv4 failover relationships between partner servers.
old-location: dhcp\dhcp_failover_relationship_array.htm
tech.root: DHCP
ms.assetid: A4C951F9-D5C6-4210-B77D-DBBD6FF2766C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, LPDHCP_FAILOVER_RELATIONSHIP_ARRAY structure pointer [DHCP], dhcp.dhcp_failover_relationship_array, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP_ARRAY'
ms.topic: struct
f1_keywords:
- dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY
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
- DHCP_FAILOVER_RELATIONSHIP_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_FAILOVER_RELATIONSHIP_ARRAY, *LPDHCP_FAILOVER_RELATIONSHIP_ARRAY
req.redist: 
ms.custom: 19H1
---

# DHCP_FAILOVER_RELATIONSHIP_ARRAY structure


## -description


The <b>DHCP_FAILOVER_RELATIONSHIP_ARRAY</b> structure defines an array of DHCPv4 failover relationships between partner servers.


## -struct-fields




### -field NumElements

 


### -field pRelationships

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a>  structures.


### -field pRelationships.size_is

 


### -field pRelationships.size_is.NumElements

 




#### - numElements

Integer that specifies the number of DHCPv4 failover relationships in <b>pRelationships.</b>


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverenumrelationship">DhcpV4FailoverEnumRelationship</a>
 

 

