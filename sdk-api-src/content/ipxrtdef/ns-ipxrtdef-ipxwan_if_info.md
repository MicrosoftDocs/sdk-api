---
UID: NS:ipxrtdef._IPXWAN_IF_INFO
title: IPXWAN_IF_INFO (ipxrtdef.h)
author: windows-sdk-content
description: The IPXWAN_IF_INFO structure stores the administrative state for an IPX WAN interface.
old-location: rras\ipxwan_if_info.htm
tech.root: RRAS
ms.assetid: c28ef4c9-ba7d-429a-ba43-82bfc9c7c58b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIPXWAN_IF_INFO, IPXWAN_IF_INFO, IPXWAN_IF_INFO structure [RAS], PIPXWAN_IF_INFO, PIPXWAN_IF_INFO structure pointer [RAS], _mpr_ipxwan_if_info, ipxrtdef/IPXWAN_IF_INFO, ipxrtdef/PIPXWAN_IF_INFO, rras.ipxwan_if_info"
ms.topic: struct
req.header: ipxrtdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Ipxrtdef.h
api_name:
 - IPXWAN_IF_INFO
product: Windows
targetos: Windows
req.typenames: IPXWAN_IF_INFO, *PIPXWAN_IF_INFO
req.redist: 
ms.custom: 19H1
---

# IPXWAN_IF_INFO structure


## -description


The 
<b>IPXWAN_IF_INFO</b> structure stores the administrative state for an IPX WAN interface.


## -struct-fields




### -field AdminState

Specifies the administrative state of the interface. This member can be one of the following values. These value are defined in Ipxconst.h. 




ADMIN_STATE_DISABLED

ADMIN_STATE_ENABLED

ADMIN_STATE_ENABLED_ONLY_FOR_NETBIOS_STATIC_ROUTING

ADMIN_STATE_ENABLED_ONLY_FOR_OPER_STATE_UP


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ipxrtdef/ns-ipxrtdef-_ipx_if_info">IPX_IF_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>
 

 

