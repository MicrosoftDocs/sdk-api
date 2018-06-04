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

# tagNC_ADDRESS structure


## -description


Contains information that describes a network address.


## -struct-fields




### -field pAddrInfo

Type: <b><a href="https://msdn.microsoft.com/1fcb7cf5-2eff-4ff8-8cb4-00ce8dddc081">NET_ADDRESS_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/1fcb7cf5-2eff-4ff8-8cb4-00ce8dddc081">NET_ADDRESS_INFO</a>  structure that describes the network address, either a named address or an IP address.


### -field PortNumber

Type: <b>USHORT</b>

The network port number, if the address described by <b>pAddrInfo</b> is an IP address.


### -field PrefixLength

Type: <b>BYTE</b>

The prefix length corresponding to the address, if the address described by <b>pAddrInfo</b> is an IP address.


## -remarks



This structure is sent with the <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a> macro.



