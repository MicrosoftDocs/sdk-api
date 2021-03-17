---
UID: NS:stm._IPX_SERVER_ENTRY
title: IPX_SERVER_ENTRY (stm.h)
description: The IPX_SERVER_ENTRY structure describes a particular IPX service.
helpviewer_keywords: ["*PIPX_SERVER_ENTRY","IPX_SERVER_ENTRY","IPX_SERVER_ENTRY structure [RAS]","PIPX_SERVER_ENTRY","PIPX_SERVER_ENTRY structure pointer [RAS]","_mpr_ipx_server_entry","rras.ipx_server_entry","stm/IPX_SERVER_ENTRY","stm/PIPX_SERVER_ENTRY"]
old-location: rras\ipx_server_entry.htm
tech.root: RRAS
ms.assetid: 5b865c28-6a0e-4af3-a646-c1082b5c3ce5
ms.date: 12/05/2018
ms.keywords: '*PIPX_SERVER_ENTRY, IPX_SERVER_ENTRY, IPX_SERVER_ENTRY structure [RAS], PIPX_SERVER_ENTRY, PIPX_SERVER_ENTRY structure pointer [RAS], _mpr_ipx_server_entry, rras.ipx_server_entry, stm/IPX_SERVER_ENTRY, stm/PIPX_SERVER_ENTRY'
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
targetos: Windows
req.typenames: IPX_SERVER_ENTRY, *PIPX_SERVER_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_SERVER_ENTRY
 - stm/_IPX_SERVER_ENTRY
 - PIPX_SERVER_ENTRY
 - stm/PIPX_SERVER_ENTRY
 - IPX_SERVER_ENTRY
 - stm/IPX_SERVER_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Stm.h
api_name:
 - IPX_SERVER_ENTRY
---

# IPX_SERVER_ENTRY structure


## -description

The 
<b>IPX_SERVER_ENTRY</b> structure describes a particular IPX service.

## -struct-fields

### -field Type

Contains the service type as defined by the SAP specification.

### -field Name

Contains the service name as defined by SAP specifications.

### -field Network

Contains the network number portion of the service address.

### -field Node

Contains the node number portion of the service address.

### -field Socket

Contains the socket number portion of service address.

### -field HopCount

Contains the service hop count.

## -see-also

<a href="/windows/desktop/RRAS/ipx-service-table-management">IPX Service Table Management</a>



<a href="/windows/desktop/api/stm/ns-stm-ipx_service">IPX_SERVICE</a>



<a href="/windows/desktop/RRAS/service-table-management-structures">Service Table Management Structures</a>