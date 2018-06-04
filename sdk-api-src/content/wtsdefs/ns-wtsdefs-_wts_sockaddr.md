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

# _WTS_SOCKADDR structure


## -description


Contains a socket address.


## -struct-fields




### -field sin_family

An integer index into the following structure members.


### -field u


### -field u.ipv4

An IPv4 address.


### -field u.ipv4.sin_port

Specifies a TCP or UDP port number.


### -field u.ipv4.in_addr

Specifies the IP address.


### -field u.ipv4.sin_zero

Contains an array of zeros.


### -field u.ipv6

An IPv6 address.


### -field u.ipv6.sin6_port

Specifies a TCP or UDP port number.


### -field u.ipv6.sin6_flowinfo

Contains IPv6 flow information.


### -field u.ipv6.sin6_addr

Specifies the IP address.


### -field u.ipv6.sin6_scope_id

Contains a scope ID

