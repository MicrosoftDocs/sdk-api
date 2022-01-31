---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0005
title: WTSSBX_MACHINE_STATE (tssbx.h)
description: Contains values that indicate the current state of a server.
helpviewer_keywords: ["WTSSBX_MACHINE_STATE","WTSSBX_MACHINE_STATE enumeration [Remote Desktop Services]","WTSSBX_MACHINE_STATE_READY","WTSSBX_MACHINE_STATE_SYNCHRONIZING","WTSSBX_MACHINE_STATE_UNSPEC","termserv.wtssbx_machine_state","tssbx/WTSSBX_MACHINE_STATE","tssbx/WTSSBX_MACHINE_STATE_READY","tssbx/WTSSBX_MACHINE_STATE_SYNCHRONIZING","tssbx/WTSSBX_MACHINE_STATE_UNSPEC"]
old-location: termserv\wtssbx_machine_state.htm
tech.root: TermServ
ms.assetid: 8913e159-9b97-4575-9718-6f2906896a32
ms.date: 12/05/2018
ms.keywords: WTSSBX_MACHINE_STATE, WTSSBX_MACHINE_STATE enumeration [Remote Desktop Services], WTSSBX_MACHINE_STATE_READY, WTSSBX_MACHINE_STATE_SYNCHRONIZING, WTSSBX_MACHINE_STATE_UNSPEC, termserv.wtssbx_machine_state, tssbx/WTSSBX_MACHINE_STATE, tssbx/WTSSBX_MACHINE_STATE_READY, tssbx/WTSSBX_MACHINE_STATE_SYNCHRONIZING, tssbx/WTSSBX_MACHINE_STATE_UNSPEC
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
req.typenames: WTSSBX_MACHINE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0005
 - tssbx/__MIDL_IWTSSBPlugin_0005
 - WTSSBX_MACHINE_STATE
 - tssbx/WTSSBX_MACHINE_STATE
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
 - WTSSBX_MACHINE_STATE
---

# WTSSBX_MACHINE_STATE enumeration


## -description

Contains values that indicate the current state of a server.

## -enum-fields

### -field WTSSBX_MACHINE_STATE_UNSPEC:0

The server state is unspecified.

### -field WTSSBX_MACHINE_STATE_READY:0x1

The server state is ready.

### -field WTSSBX_MACHINE_STATE_SYNCHRONIZING:0x2

The server is synchronizing with RD Connection Broker.

