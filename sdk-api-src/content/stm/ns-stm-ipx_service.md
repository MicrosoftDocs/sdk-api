---
UID: NS:stm._IPX_SERVICE
title: IPX_SERVICE (stm.h)
author: windows-sdk-content
description: The IPX_SERVICE structure contains information about an IPX service, and identifies the interface and protocol through which this information was obtained.
old-location: rras\ipx_service.htm
tech.root: RRAS
ms.assetid: 37da1071-b665-405c-a4ce-f1a484aeb19b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIPX_SERVICE, IPX_SERVICE, IPX_SERVICE structure [RAS], PIPX_SERVICE, PIPX_SERVICE structure pointer [RAS], _mpr_ipx_service, rras.ipx_service, stm/IPX_SERVICE, stm/PIPX_SERVICE"
ms.topic: struct
req.header: stm.h
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
 - Stm.h
api_name:
 - IPX_SERVICE
product: Windows
targetos: Windows
req.typenames: IPX_SERVICE, *PIPX_SERVICE
req.redist: 
ms.custom: 19H1
---

# IPX_SERVICE structure


## -description


The 
<b>IPX_SERVICE</b> structure contains information about an IPX service, and identifies the interface and protocol through which this information was obtained.


## -struct-fields




### -field InterfaceIndex

Contains the index of the interface through which the service information was obtained.


### -field Protocol

Contains the identifier of the protocol that obtained the service information. Static services are viewed as services obtained through the IPX_PROTOCOL_STATIC protocol.


### -field Server

 




#### - Service

Specifies an 
<a href="https://docs.microsoft.com/windows/desktop/api/stm/ns-stm-_ipx_server_entry">IPX_SERVER_ENTRY</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="https://docs.microsoft.com/windows/desktop/api/stm/ns-stm-_ipx_server_entry">IPX_SERVER_ENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/service-table-management-structures">Service Table Management Structures</a>
 

 

