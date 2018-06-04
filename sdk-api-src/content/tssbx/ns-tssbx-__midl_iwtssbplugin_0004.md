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

# __MIDL_IWTSSBPlugin_0004 structure


## -description


Contains information about the IP address of a network resource.


## -struct-fields




### -field AddressFamily

A value of the <a href="https://msdn.microsoft.com/8fe243ef-f52b-4b1a-8300-0b8a5a8a4c8d">WTSSBX_ADDRESS_FAMILY</a> enumeration type that indicates the address family of the network address.


### -field Address

The network address of the resource.


### -field PortNumber

The port number of the resource that is configured for Remote Desktop Protocol (RDP).


### -field dwScope

The scope of the address. This member is used only for IPv6 addresses.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

