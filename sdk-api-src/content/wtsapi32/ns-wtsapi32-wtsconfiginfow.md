---
UID: NS:wtsapi32._WTSCONFIGINFOW
title: WTSCONFIGINFOW (wtsapi32.h)
description: Contains information about a Remote Desktop Services session. (WTSCONFIGINFOW)
helpviewer_keywords: ["*PWTSCONFIGINFOW","PWTSCONFIGINFO","PWTSCONFIGINFO structure pointer [Remote Desktop Services]","WTSCONFIGINFO","WTSCONFIGINFO structure [Remote Desktop Services]","WTSCONFIGINFOA","WTSCONFIGINFOW","termserv.wtsconfiginfo","wtsapi32/PWTSCONFIGINFO","wtsapi32/WTSCONFIGINFO","wtsapi32/WTSCONFIGINFOA","wtsapi32/WTSCONFIGINFOW"]
old-location: termserv\wtsconfiginfo.htm
tech.root: TermServ
ms.assetid: 11561aee-0b73-4e4a-8a53-11a46c7838c7
ms.date: 12/05/2018
ms.keywords: '*PWTSCONFIGINFOW, PWTSCONFIGINFO, PWTSCONFIGINFO structure pointer [Remote Desktop Services], WTSCONFIGINFO, WTSCONFIGINFO structure [Remote Desktop Services], WTSCONFIGINFOA, WTSCONFIGINFOW, termserv.wtsconfiginfo, wtsapi32/PWTSCONFIGINFO, wtsapi32/WTSCONFIGINFO, wtsapi32/WTSCONFIGINFOA, wtsapi32/WTSCONFIGINFOW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSCONFIGINFOW (Unicode) and WTSCONFIGINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSCONFIGINFOW, *PWTSCONFIGINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTSCONFIGINFOW
 - wtsapi32/_WTSCONFIGINFOW
 - PWTSCONFIGINFOW
 - wtsapi32/PWTSCONFIGINFOW
 - WTSCONFIGINFOW
 - wtsapi32/WTSCONFIGINFOW
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
 - WTSCONFIGINFO
 - WTSCONFIGINFOA
 - WTSCONFIGINFOW
---

# WTSCONFIGINFOW structure


## -description

Contains information about a Remote Desktop Services session.  This structure is returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function when you specify "WTSConfigInfo" for the <i>WTSInfoClass</i> parameter.

## -struct-fields

### -field version

This member is reserved.

### -field fConnectClientDrivesAtLogon

This member is reserved.

### -field fConnectPrinterAtLogon

This member is reserved.

### -field fDisablePrinterRedirection

Specifies whether the client can use printer redirection.



#### 0

Enable client printer redirection.



#### 1

Disable client printer redirection.

### -field fDisableDefaultMainClientPrinter

Specifies whether the printer connected to the client is the default printer for the user.



#### 0

The printer connected to the client is not the default printer for the user.



#### 1

The printer connected to the client is the default printer for the user.

### -field ShadowSettings

The remote control setting. Remote control allows a user to remotely monitor the on-screen operations of another user. This member can be one of the following values.



#### 0

Remote control is disabled.



#### 1

The user of remote control has full control of the user's session, with the user's permission.



#### 2

The user of remote control has full control of the user's session; the user's permission is 
        not required.



#### 3

The user of remote control can view the session remotely, with the user's permission; the remote user 
        cannot actively control the session.



#### 4

The user of remote control can view the session remotely but not actively control the session; the 
        user's permission is not required.

### -field LogonUserName

A null-terminated string that contains the user name used in automatic logon scenarios.

### -field LogonDomain

A null-terminated string that contains the domain name used in automatic logon scenarios.

### -field WorkDirectory

A null-terminated string that contains the path of the working directory of  the initial program.

### -field InitialProgram

A null-terminated string that contains the name of  the program to start immediately after the user logs on to the server.

### -field ApplicationName

This member is reserved.


##### - ShadowSettings.0

Remote control is disabled.


##### - ShadowSettings.1

The user of remote control has full control of the user's session, with the user's permission.


##### - ShadowSettings.2

The user of remote control has full control of the user's session; the user's permission is 
        not required.


##### - ShadowSettings.3

The user of remote control can view the session remotely, with the user's permission; the remote user 
        cannot actively control the session.


##### - ShadowSettings.4

The user of remote control can view the session remotely but not actively control the session; the 
        user's permission is not required.


##### - fDisableDefaultMainClientPrinter.0

The printer connected to the client is not the default printer for the user.


##### - fDisableDefaultMainClientPrinter.1

The printer connected to the client is the default printer for the user.


##### - fDisablePrinterRedirection.0

Enable client printer redirection.


##### - fDisablePrinterRedirection.1

Disable client printer redirection.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTSCONFIGINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
