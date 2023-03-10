---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0006
title: WTSSBX_MACHINE_CONNECT_INFO (tssbx.h)
description: Contains information about a computer that is accepting remote connections.
helpviewer_keywords: ["WTSSBX_MACHINE_CONNECT_INFO","WTSSBX_MACHINE_CONNECT_INFO structure [Remote Desktop Services]","__MIDL_IWTSSBPlugin_0006","termserv.wtssbx_machine_connect_info","tssbx/WTSSBX_MACHINE_CONNECT_INFO"]
old-location: termserv\wtssbx_machine_connect_info.htm
tech.root: TermServ
ms.assetid: 805e606b-6f30-4f49-af04-b7f298c4fadf
ms.date: 12/05/2018
ms.keywords: WTSSBX_MACHINE_CONNECT_INFO, WTSSBX_MACHINE_CONNECT_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0006, termserv.wtssbx_machine_connect_info, tssbx/WTSSBX_MACHINE_CONNECT_INFO
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
req.typenames: WTSSBX_MACHINE_CONNECT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0006
 - tssbx/__MIDL_IWTSSBPlugin_0006
 - WTSSBX_MACHINE_CONNECT_INFO
 - tssbx/WTSSBX_MACHINE_CONNECT_INFO
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
 - WTSSBX_MACHINE_CONNECT_INFO
---

# WTSSBX_MACHINE_CONNECT_INFO structure


## -description

Contains information about a computer that is accepting remote connections.

## -struct-fields

### -field wczMachineFQDN

The fully qualified domain name (FQDN) of the computer.  The name cannot exceed 256 characters.

### -field wczMachineNetBiosName

The NetBIOS name of the computer. The name cannot exceed 16 characters.

### -field dwNumOfIPAddr

The number of IP addresses that are configured on the computer.

### -field IPaddr

An array of <a href="/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address">WTSSBX_IP_ADDRESS</a> structures that indicate the IP addresses on this computer that are visible to Remote Desktop Connection (RDC) clients. This array cannot exceed 12 elements.

## -see-also

<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>