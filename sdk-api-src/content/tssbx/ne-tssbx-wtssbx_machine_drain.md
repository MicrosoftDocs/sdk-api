---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0001
title: WTSSBX_MACHINE_DRAIN (tssbx.h)
description: Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.
helpviewer_keywords: ["WTSSBX_MACHINE_DRAIN","WTSSBX_MACHINE_DRAIN enumeration [Remote Desktop Services]","WTSSBX_MACHINE_DRAIN_OFF","WTSSBX_MACHINE_DRAIN_ON","WTSSBX_MACHINE_DRAIN_UNSPEC","termserv.wtssbx_machine_drain","tssbx/WTSSBX_MACHINE_DRAIN","tssbx/WTSSBX_MACHINE_DRAIN_OFF","tssbx/WTSSBX_MACHINE_DRAIN_ON","tssbx/WTSSBX_MACHINE_DRAIN_UNSPEC"]
old-location: termserv\wtssbx_machine_drain.htm
tech.root: TermServ
ms.assetid: 251d1534-0571-427a-a9a1-2327eba55c2d
ms.date: 12/05/2018
ms.keywords: WTSSBX_MACHINE_DRAIN, WTSSBX_MACHINE_DRAIN enumeration [Remote Desktop Services], WTSSBX_MACHINE_DRAIN_OFF, WTSSBX_MACHINE_DRAIN_ON, WTSSBX_MACHINE_DRAIN_UNSPEC, termserv.wtssbx_machine_drain, tssbx/WTSSBX_MACHINE_DRAIN, tssbx/WTSSBX_MACHINE_DRAIN_OFF, tssbx/WTSSBX_MACHINE_DRAIN_ON, tssbx/WTSSBX_MACHINE_DRAIN_UNSPEC
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
req.typenames: WTSSBX_MACHINE_DRAIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0001
 - tssbx/__MIDL_IWTSSBPlugin_0001
 - WTSSBX_MACHINE_DRAIN
 - tssbx/WTSSBX_MACHINE_DRAIN
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
 - WTSSBX_MACHINE_DRAIN
---

# WTSSBX_MACHINE_DRAIN enumeration


## -description

Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server. The drain state indicates whether an RD Session Host server is accepting new connections. If the RD Session Host server is currently accepting new connections,  its drain state is off. If it is not accepting new connections, its drain state is on.

## -enum-fields

### -field WTSSBX_MACHINE_DRAIN_UNSPEC:0

The drain state of the server is unspecified.

### -field WTSSBX_MACHINE_DRAIN_OFF:0x1

The server is accepting new user sessions.

### -field WTSSBX_MACHINE_DRAIN_ON:0x2

The server is not accepting new user sessions.

