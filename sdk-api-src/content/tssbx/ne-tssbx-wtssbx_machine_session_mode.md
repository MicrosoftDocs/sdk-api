---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0002
title: WTSSBX_MACHINE_SESSION_MODE (tssbx.h)
description: Contains values that indicate the session mode of a Remote Desktop Session Host (RD Session Host) server.
helpviewer_keywords: ["WTSSBX_MACHINE_SESSION_MODE","WTSSBX_MACHINE_SESSION_MODE enumeration [Remote Desktop Services]","WTSSBX_MACHINE_SESSION_MODE_MULTIPLE","WTSSBX_MACHINE_SESSION_MODE_SINGLE","WTSSBX_MACHINE_SESSION_MODE_UNSPEC","termserv.wtssbx_machine_session_mode","tssbx/WTSSBX_MACHINE_SESSION_MODE","tssbx/WTSSBX_MACHINE_SESSION_MODE_MULTIPLE","tssbx/WTSSBX_MACHINE_SESSION_MODE_SINGLE","tssbx/WTSSBX_MACHINE_SESSION_MODE_UNSPEC"]
old-location: termserv\wtssbx_machine_session_mode.htm
tech.root: TermServ
ms.assetid: 38894819-a39f-4c1f-aef9-ec3036b42877
ms.date: 12/05/2018
ms.keywords: WTSSBX_MACHINE_SESSION_MODE, WTSSBX_MACHINE_SESSION_MODE enumeration [Remote Desktop Services], WTSSBX_MACHINE_SESSION_MODE_MULTIPLE, WTSSBX_MACHINE_SESSION_MODE_SINGLE, WTSSBX_MACHINE_SESSION_MODE_UNSPEC, termserv.wtssbx_machine_session_mode, tssbx/WTSSBX_MACHINE_SESSION_MODE, tssbx/WTSSBX_MACHINE_SESSION_MODE_MULTIPLE, tssbx/WTSSBX_MACHINE_SESSION_MODE_SINGLE, tssbx/WTSSBX_MACHINE_SESSION_MODE_UNSPEC
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
req.typenames: WTSSBX_MACHINE_SESSION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IWTSSBPlugin_0002
 - tssbx/__MIDL_IWTSSBPlugin_0002
 - WTSSBX_MACHINE_SESSION_MODE
 - tssbx/WTSSBX_MACHINE_SESSION_MODE
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
 - WTSSBX_MACHINE_SESSION_MODE
---

# WTSSBX_MACHINE_SESSION_MODE enumeration


## -description

Contains values that indicate the session mode of a Remote Desktop Session Host (RD Session Host) server.

## -enum-fields

### -field WTSSBX_MACHINE_SESSION_MODE_UNSPEC:0

The session mode of the server is unspecified.

### -field WTSSBX_MACHINE_SESSION_MODE_SINGLE:0x1

The server is in single session mode. It can only accept one session per user.

### -field WTSSBX_MACHINE_SESSION_MODE_MULTIPLE:0x2

The server is in multiple session mode. It can accept multiple sessions per user.

