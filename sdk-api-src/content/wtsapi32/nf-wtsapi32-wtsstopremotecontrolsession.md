---
UID: NF:wtsapi32.WTSStopRemoteControlSession
title: WTSStopRemoteControlSession function (wtsapi32.h)
description: Stops a remote control session.
helpviewer_keywords: ["WTSStopRemoteControlSession","WTSStopRemoteControlSession function [Remote Desktop Services]","termserv.wtsstopremotecontrolsession","wtsapi32/WTSStopRemoteControlSession"]
old-location: termserv\wtsstopremotecontrolsession.htm
tech.root: TermServ
ms.assetid: 65e5b584-4ffc-4b89-992e-7ada7df0262b
ms.date: 12/05/2018
ms.keywords: WTSStopRemoteControlSession, WTSStopRemoteControlSession function [Remote Desktop Services], termserv.wtsstopremotecontrolsession, wtsapi32/WTSStopRemoteControlSession
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSStopRemoteControlSession
 - wtsapi32/WTSStopRemoteControlSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSStopRemoteControlSession
---

# WTSStopRemoteControlSession function


## -description

Stops a remote control session.

## -parameters

### -param LogonId [in]

The logon ID of the session that you want to stop the remote control of.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.