---
UID: NE:tssbx.__MIDL_IWTSSBPlugin_0002
title: "__MIDL_IWTSSBPlugin_0002"
author: windows-sdk-content
description: Contains values that indicate the session mode of a Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtssbx_machine_session_mode.htm
old-project: TermServ
ms.assetid: 38894819-a39f-4c1f-aef9-ec3036b42877
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WTSSBX_MACHINE_SESSION_MODE, WTSSBX_MACHINE_SESSION_MODE enumeration [Remote Desktop Services], WTSSBX_MACHINE_SESSION_MODE_MULTIPLE, WTSSBX_MACHINE_SESSION_MODE_SINGLE, WTSSBX_MACHINE_SESSION_MODE_UNSPEC, __MIDL_IWTSSBPlugin_0002, termserv.wtssbx_machine_session_mode, tssbx/WTSSBX_MACHINE_SESSION_MODE, tssbx/WTSSBX_MACHINE_SESSION_MODE_MULTIPLE, tssbx/WTSSBX_MACHINE_SESSION_MODE_SINGLE, tssbx/WTSSBX_MACHINE_SESSION_MODE_UNSPEC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WTSSBX_MACHINE_SESSION_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_MACHINE_SESSION_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL_IWTSSBPlugin_0002 enumeration


## -description


Contains values that indicate the session mode of a Remote Desktop Session Host (RD Session Host) server.


## -enum-fields




### -field WTSSBX_MACHINE_SESSION_MODE_UNSPEC

The session mode of the server is unspecified.


### -field WTSSBX_MACHINE_SESSION_MODE_SINGLE

The server is in single session mode. It can only accept one session per user.


### -field WTSSBX_MACHINE_SESSION_MODE_MULTIPLE

The server is in multiple session mode. It can accept multiple sessions per user.

