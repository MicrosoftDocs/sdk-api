---
UID: NS:dhcpsapi._DHCP_FAILOVER_RELATIONSHIP_ARRAY
title: "_DHCP_FAILOVER_RELATIONSHIP_ARRAY"
author: windows-sdk-content
description: The DHCP_FAILOVER_RELATIONSHIP_ARRAY structure defines an array of DHCPv4 failover relationships between partner servers.
old-location: dhcp\dhcp_failover_relationship_array.htm
old-project: dhcp
ms.assetid: A4C951F9-D5C6-4210-B77D-DBBD6FF2766C
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY, DHCP_FAILOVER_RELATIONSHIP_ARRAY structure [DHCP], LPDHCP_FAILOVER_RELATIONSHIP_ARRAY, LPDHCP_FAILOVER_RELATIONSHIP_ARRAY structure pointer [DHCP], _DHCP_FAILOVER_RELATIONSHIP_ARRAY, dhcp.dhcp_failover_relationship_array, dhcpsapi/DHCP_FAILOVER_RELATIONSHIP_ARRAY, dhcpsapi/LPDHCP_FAILOVER_RELATIONSHIP_ARRAY"
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
tech.root: 
req.typenames: DHCP_FAILOVER_RELATIONSHIP_ARRAY, *LPDHCP_FAILOVER_RELATIONSHIP_ARRAY
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
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FAILOVER_RELATIONSHIP_ARRAY structure


## -description


The <b>DHCP_FAILOVER_RELATIONSHIP_ARRAY</b> structure defines an array of DHCPv4 failover relationships between partner servers.


## -struct-fields




### -field NumElements

 


### -field pRelationships

Pointer to an array of <a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a>  structures.


### -field pRelationships.size_is

 


### -field pRelationships.size_is.NumElements

 




#### - numElements

Integer that specifies the number of DHCPv4 failover relationships in <b>pRelationships.</b>


## -see-also




<a href="https://msdn.microsoft.com/81ef2af8-c1a9-44e7-857c-1591947609ed">DhcpV4FailoverEnumRelationship</a>
 

 

