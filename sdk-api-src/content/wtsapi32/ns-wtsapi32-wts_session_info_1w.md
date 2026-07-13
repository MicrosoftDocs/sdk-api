---
UID: NS:wtsapi32._WTS_SESSION_INFO_1W
title: WTS_SESSION_INFO_1W (wtsapi32.h)
description: Contains extended information about a client session on a Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server. (Unicode)
helpviewer_keywords: ["*PWTS_SESSION_INFO_1W","PWTS_SESSION_INFO_1","PWTS_SESSION_INFO_1 structure pointer [Remote Desktop Services]","WTS_SESSION_INFO_1","WTS_SESSION_INFO_1 structure [Remote Desktop Services]","WTS_SESSION_INFO_1A","WTS_SESSION_INFO_1W","termserv.wts_session_info_1","wtsapi32/PWTS_SESSION_INFO_1","wtsapi32/WTS_SESSION_INFO_1","wtsapi32/WTS_SESSION_INFO_1A","wtsapi32/WTS_SESSION_INFO_1W"]
old-location: termserv\wts_session_info_1.htm
tech.root: TermServ
ms.assetid: 29d76033-d61d-4bc5-b47a-f7dea9543f23
ms.date: 12/05/2018
ms.keywords: '*PWTS_SESSION_INFO_1W, PWTS_SESSION_INFO_1, PWTS_SESSION_INFO_1 structure pointer [Remote Desktop Services], WTS_SESSION_INFO_1, WTS_SESSION_INFO_1 structure [Remote Desktop Services], WTS_SESSION_INFO_1A, WTS_SESSION_INFO_1W, termserv.wts_session_info_1, wtsapi32/PWTS_SESSION_INFO_1, wtsapi32/WTS_SESSION_INFO_1, wtsapi32/WTS_SESSION_INFO_1A, wtsapi32/WTS_SESSION_INFO_1W'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_SESSION_INFO_1W (Unicode) and WTS_SESSION_INFO_1A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_SESSION_INFO_1W, *PWTS_SESSION_INFO_1W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SESSION_INFO_1W
 - wtsapi32/_WTS_SESSION_INFO_1W
 - PWTS_SESSION_INFO_1W
 - wtsapi32/PWTS_SESSION_INFO_1W
 - WTS_SESSION_INFO_1W
 - wtsapi32/WTS_SESSION_INFO_1W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_SESSION_INFO_1
 - WTS_SESSION_INFO_1A
 - WTS_SESSION_INFO_1W
---

# WTS_SESSION_INFO_1W structure


## -description

Contains 
    extended information about a client session on a Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.

## -struct-fields

### -field ExecEnvId

An identifier that uniquely identifies the session within the list of sessions returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa">WTSEnumerateSessionsEx</a> function. For more information, see Remarks.

### -field State

A value of the <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a> enumeration type that specifies the connection state of a Remote Desktop Services session.

### -field SessionId

A session identifier assigned by the RD Session Host server, RD Virtualization Host server, or virtual machine.

### -field pSessionName

A pointer to a null-terminated string that contains the name of this session. For example, "services", "console", or "RDP-Tcp#0".

### -field pHostName

A pointer to a null-terminated string that contains the name of the computer that the session is running on. If the session is running directly on an RD Session Host server or RD Virtualization Host server, the string contains <b>NULL</b>. If the session is running on a virtual machine, the string contains the name of the virtual machine.

### -field pUserName

A pointer to a null-terminated string that contains the name of the user who is logged on to the session. If no user is logged on to the session, the string contains <b>NULL</b>.

### -field pDomainName

A pointer to a null-terminated string that contains the domain name of the user who is logged on to the session. If no user is logged on to the session, the string contains <b>NULL</b>.

### -field pFarmName

A pointer to a null-terminated string that contains the name of the farm that the virtual machine is joined to.  If the session is not running on a virtual machine that is joined to a farm, the string contains <b>NULL</b>.

## -remarks

The <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa">WTSEnumerateSessionsEx</a> function returns this structure if you call the function and specify a handle to an RD Virtualization Host server  that you obtained by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function. In this case, the <b>WTSEnumerateSessionsEx</b> function aggregates all the sessions running on the host itself as well as sessions running on individual virtual machines.  The <i>ExecEnvId</i> parameter uniquely identifies each session in the aggregated list. This identifier may be different from the actual session identifier defined in the server or virtual machine that hosts the session, which is specified by the <b>SessionId</b> member.

The session represented by this structure could be a session running directly on the server or a session running within a virtual machine. If the session is running within a virtual machine, the <b>pHostName</b> member contains the name of the virtual machine. The <b>pFarmName</b> member is applicable to sessions that are hosted on virtual machines that are joined to a RD Session Host farm.





> [!NOTE]
> The wtsapi32.h header defines WTS_SESSION_INFO_1 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa">WTSEnumerateSessionsEx</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_infoa">WTS_SESSION_INFO</a>
