---
UID: NS:dhcpsapi.DHCPV6_STATELESS_PARAMS
title: DHCPV6_STATELESS_PARAMS
author: windows-sdk-content
description: The DHCPV6_STATELESS_PARAMS structure defines the DHCPv6 stateless client inventory configuration settings at server and scope level.
old-location: dhcp\dhcpv6_stateless_params.htm
tech.root: dhcp
ms.assetid: 852249b2-ea0d-4f83-a41f-12ef8cb029e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCPV6_STATELESS_PARAMS, *PDHCPV6_STATELESS_PARAMS, DHCPV6_STATELESS_PARAMS, DHCPV6_STATELESS_PARAMS structure [DHCP], LPDHCPV6_STATELESS_PARAMS, LPDHCPV6_STATELESS_PARAMS structure pointer [DHCP], PDHCPV6_STATELESS_PARAMS, PDHCPV6_STATELESS_PARAMS structure pointer [DHCP], dhcp.dhcpv6_stateless_params, dhcpsapi/DHCPV6_STATELESS_PARAMS, dhcpsapi/LPDHCPV6_STATELESS_PARAMS, dhcpsapi/PDHCPV6_STATELESS_PARAMS"
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
 - DHCPV6_STATELESS_PARAMS
product: Windows
targetos: Windows
req.typenames: DHCPV6_STATELESS_PARAMS, *PDHCPV6_STATELESS_PARAMS, *LPDHCPV6_STATELESS_PARAMS
req.redist: 
---

# DHCPV6_STATELESS_PARAMS structure


## -description


The <b>DHCPV6_STATELESS_PARAMS</b> structure defines the DHCPv6 stateless client inventory configuration settings at server and scope level.


## -struct-fields




### -field Status

If <b>TRUE</b> the stateless client inventory is maintained by the DHCPv6 server. Otherwise, it is  <b>FALSE</b>. The default value is <b>FALSE</b>, which indicates that the stateless client inventory is disabled and is not maintained the by the server.


### -field PurgeInterval

Integer that specifies the maximum time interval, in hours, that stateless IPv6 DHCP client lease records can persist before being deleted from the DHCP server database.


## -see-also




<a href="https://msdn.microsoft.com/8670c69b-1fc0-4b60-b5cc-a616d56c9319">DHCPV6_STATELESS_PARAM_TYPE</a>



<a href="https://msdn.microsoft.com/80a32132-a032-452f-9438-52a1eb280fdf">Dhcpv6GetStatelessStoreParams</a>



<a href="https://msdn.microsoft.com/8f64c1bb-8f02-45e3-b9ed-8fce2bf9885c">Dhcpv6SetStatelessStoreParams</a>
 

 

