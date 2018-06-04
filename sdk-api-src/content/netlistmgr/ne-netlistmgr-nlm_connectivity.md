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

# NLM_CONNECTIVITY enumeration


## -description


The NLM_Connectivity enumeration is  a set of flags that provide notification whenever connectivity related parameters have changed. 


## -enum-fields




### -field NLM_CONNECTIVITY_DISCONNECTED

The underlying network interfaces have no connectivity to any network.


### -field NLM_CONNECTIVITY_IPV4_NOTRAFFIC

There is connectivity to a network, but the service cannot detect any IPv4 Network Traffic.


### -field NLM_CONNECTIVITY_IPV6_NOTRAFFIC

There is connectivity to a network, but the service cannot detect any IPv6 Network Traffic.


### -field NLM_CONNECTIVITY_IPV4_SUBNET

There is connectivity to the local subnet using the IPv4 protocol.


### -field NLM_CONNECTIVITY_IPV4_LOCALNETWORK

There is connectivity to a routed network using the IPv4 protocol.


### -field NLM_CONNECTIVITY_IPV4_INTERNET

There is connectivity to the Internet using the IPv4 protocol.


### -field NLM_CONNECTIVITY_IPV6_SUBNET

There is connectivity to the local subnet using the IPv6 protocol.


### -field NLM_CONNECTIVITY_IPV6_LOCALNETWORK

There is connectivity to a local network using the IPv6 protocol.


### -field NLM_CONNECTIVITY_IPV6_INTERNET

There is connectivity to the Internet using the IPv6 protocol.

