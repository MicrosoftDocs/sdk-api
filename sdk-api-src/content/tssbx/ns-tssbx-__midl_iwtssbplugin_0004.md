---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0004
title: "__MIDL_IWTSSBPlugin_0004"
author: windows-sdk-content
description: Contains information about the IP address of a network resource.
old-location: termserv\wtssbx_ip_address.htm
old-project: TermServ
ms.assetid: 92fe662a-ad31-4ed3-9393-c7d86f97e702
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WTSSBX_IP_ADDRESS, WTSSBX_IP_ADDRESS structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0004, termserv.wtssbx_ip_address, tssbx/WTSSBX_IP_ADDRESS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTSSBX_IP_ADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_IP_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

