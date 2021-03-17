---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0004
title: WTSSBX_IP_ADDRESS (tssbx.h)
description: Contains information about the IP address of a network resource.
helpviewer_keywords: ["WTSSBX_IP_ADDRESS","WTSSBX_IP_ADDRESS structure [Remote Desktop Services]","__MIDL_IWTSSBPlugin_0004","termserv.wtssbx_ip_address","tssbx/WTSSBX_IP_ADDRESS"]
old-location: termserv\wtssbx_ip_address.htm
tech.root: TermServ
ms.assetid: 92fe662a-ad31-4ed3-9393-c7d86f97e702
ms.date: 12/05/2018
ms.keywords: WTSSBX_IP_ADDRESS, WTSSBX_IP_ADDRESS structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0004, termserv.wtssbx_ip_address, tssbx/WTSSBX_IP_ADDRESS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSSBX_IP_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0004
 - tssbx/__MIDL_IWTSSBPlugin_0004
 - WTSSBX_IP_ADDRESS
 - tssbx/WTSSBX_IP_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_IP_ADDRESS
---

# WTSSBX_IP_ADDRESS structure


## -description

Contains information about the IP address of a network resource.

## -struct-fields

### -field AddressFamily

A value of the <a href="/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family">WTSSBX_ADDRESS_FAMILY</a> enumeration type that indicates the address family of the network address.

### -field Address

The network address of the resource.

### -field PortNumber

The port number of the resource that is configured for Remote Desktop Protocol (RDP).

### -field dwScope

The scope of the address. This member is used only for IPv6 addresses.

## -see-also

<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>