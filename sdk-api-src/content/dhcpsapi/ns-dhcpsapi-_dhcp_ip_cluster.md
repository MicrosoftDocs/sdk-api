---
UID: NS:dhcpsapi._DHCP_IP_CLUSTER
title: "_DHCP_IP_CLUSTER"
author: windows-driver-content
description: The DHCP_IP_CLUSTER structure defines the address and mast for a network cluster.
old-location: dhcp\dhcp_ip_cluster.htm
old-project: DHCP
ms.assetid: 6dad62c3-c56f-4526-ae5c-dbb74cb13c8f
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCP_IP_CLUSTER, DHCP_IP_CLUSTER, DHCP_IP_CLUSTER structure [DHCP], LPDHCP_IP_CLUSTER, LPDHCP_IP_CLUSTER structure pointer [DHCP], _DHCP_IP_CLUSTER, dhcp.dhcp_ip_cluster, dhcpsapi/LPDHCP_IP_CLUSTER, dhcpsapi/_DHCP_IP_CLUSTER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_IP_CLUSTER, *LPDHCP_IP_CLUSTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_IP_CLUSTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_IP_CLUSTER structure


## -description


The <b>DHCP_IP_CLUSTER</b> structure defines the address and mast for a network cluster.


## -struct-fields




### -field ClusterAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the cluster.


### -field ClusterMask

Specifies the mask value for a cluster. This value should be set to  0xFFFFFFFF if the cluster is full.

