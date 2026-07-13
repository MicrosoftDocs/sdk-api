---
UID: NF:wtsapi32.WTSConnectSessionW
title: WTSConnectSessionW function (wtsapi32.h)
description: Connects a Remote Desktop Services session to an existing session on the local computer. (Unicode)
helpviewer_keywords: ["WTSConnectSession", "WTSConnectSession function [Remote Desktop Services]", "WTSConnectSessionW", "termserv.wtsconnectsession", "wtsapi32/WTSConnectSession", "wtsapi32/WTSConnectSessionW"]
old-location: termserv\wtsconnectsession.htm
tech.root: TermServ
ms.assetid: 3911b02c-43df-4a8d-9cd6-92d2e5323f61
ms.date: 12/05/2018
ms.keywords: WTSConnectSession, WTSConnectSession function [Remote Desktop Services], WTSConnectSessionA, WTSConnectSessionW, termserv.wtsconnectsession, wtsapi32/WTSConnectSession, wtsapi32/WTSConnectSessionA, wtsapi32/WTSConnectSessionW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSConnectSessionW (Unicode) and WTSConnectSessionA (ANSI)
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
 - WTSConnectSessionW
 - wtsapi32/WTSConnectSessionW
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
 - WTSConnectSession
 - WTSConnectSessionA
 - WTSConnectSessionW
---

# WTSConnectSessionW function


## -description

Connects a Remote Desktop Services session to an existing session on the local computer.

## -parameters

### -param LogonId [in]

The logon ID of the session to connect to. The user of that session must have permissions to connect to an existing session. The output of this session will be routed to the session identified by the <i>TargetLogonId</i> parameter.

This can be <b>LOGONID_CURRENT</b> to use the current session.

### -param TargetLogonId [in]

The logon ID of the session to receive the output of the session represented by the <i>LogonId</i> parameter. The output of the session identified by the <i>LogonId</i> parameter will be routed to this session.

This can be <b>LOGONID_CURRENT</b> to use the current session.

### -param pPassword [in]

A pointer to the password for the user account that is specified in the <i>LogonId</i> parameter. The value of <i>pPassword</i> can be an empty string if the caller is logged on using the same domain name and user name as the logon ID. The value of <i>pPassword</i> cannot be <b>NULL</b>.

### -param bWait [in]

Indicates whether the operation is synchronous. Specify <b>TRUE</b> to wait for the operation to complete, or <b>FALSE</b> to return immediately.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Either the <i>LogonId</i> or <i>TargetLogonId</i> parameter can be <b>LOGONID_CURRENT</b>, but not both.




> [!NOTE]
> The wtsapi32.h header defines WTSConnectSession as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
