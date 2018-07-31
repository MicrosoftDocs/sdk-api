---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0006
title: "__MIDL_IWTSSBPlugin_0006"
author: windows-sdk-content
description: Contains information about a computer that is accepting remote connections.
old-location: termserv\wtssbx_machine_connect_info.htm
old-project: TermServ
ms.assetid: 805e606b-6f30-4f49-af04-b7f298c4fadf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WTSSBX_MACHINE_CONNECT_INFO, WTSSBX_MACHINE_CONNECT_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0006, termserv.wtssbx_machine_connect_info, tssbx/WTSSBX_MACHINE_CONNECT_INFO
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
req.typenames: WTSSBX_MACHINE_CONNECT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_MACHINE_CONNECT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL_IWTSSBPlugin_0006 structure


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

An array of <a href="https://msdn.microsoft.com/92fe662a-ad31-4ed3-9393-c7d86f97e702">WTSSBX_IP_ADDRESS</a> structures that indicate the IP addresses on this computer that are visible to Remote Desktop Connection (RDC) clients. This array cannot exceed 12 elements.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

