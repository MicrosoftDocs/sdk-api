---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DHCP_SERVER_CONFIG_INFO_V6 structure


## -description


The <b>DHCP_SERVER_CONFIG_INFO_V6</b> structure contains the settings for the DHCPv6 server.


## -struct-fields




### -field UnicastFlag

Reserved. This must to be set to 0.


### -field RapidCommitFlag

Reserved. This must to be set to 0.


### -field PreferredLifetime

Integer value that specifies the preferred lifetime for IANA addresses.


### -field ValidLifetime

Integer value that specifies the valid lifetime for IANA addresses.


### -field T1

Integer that specifies the value for time T1.


### -field T2

Integer that specifies the value for time T2.


### -field PreferredLifetimeIATA

The preferred lifetime value for a temporary IPv6 address. This is not used, and must to be set to 0.


### -field ValidLifetimeIATA

The valid lifetime value for a temporary IPv6 address. This is not used, and must to be set to 0.


### -field fAuditLog

If <b>TRUE</b>, audit logs are enabled on the DHCPv6 server; if <b>FALSE</b>, they are not.

