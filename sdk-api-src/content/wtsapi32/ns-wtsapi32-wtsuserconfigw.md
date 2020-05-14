---
UID: NS:wtsapi32._WTSUSERCONFIGW
title: WTSUSERCONFIGW (wtsapi32.h)
description: Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.helpviewer_keywords: ["*PWTSUSERCONFIGW","PWTSUSERCONFIG","PWTSUSERCONFIG structure pointer [Remote Desktop Services]","WTSUSERCONFIG","WTSUSERCONFIG structure [Remote Desktop Services]","WTSUSERCONFIGA","WTSUSERCONFIGW","termserv.wtsuserconfig","wtsapi32/PWTSUSERCONFIG","wtsapi32/WTSUSERCONFIG","wtsapi32/WTSUSERCONFIGA","wtsapi32/WTSUSERCONFIGW"]
old-location: termserv\wtsuserconfig.htm
tech.root: TermServ
ms.assetid: 73788ea3-1ba7-4749-983d-4ca6e4f76acb
ms.date: 12/05/2018
ms.keywords: '*PWTSUSERCONFIGW, PWTSUSERCONFIG, PWTSUSERCONFIG structure pointer [Remote Desktop Services], WTSUSERCONFIG, WTSUSERCONFIG structure [Remote Desktop Services], WTSUSERCONFIGA, WTSUSERCONFIGW, termserv.wtsuserconfig, wtsapi32/PWTSUSERCONFIG, wtsapi32/WTSUSERCONFIG, wtsapi32/WTSUSERCONFIGA, wtsapi32/WTSUSERCONFIGW'
f1_keywords:
- wtsapi32/WTSUSERCONFIG
dev_langs:
- c++
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSUSERCONFIGW (Unicode) and WTSUSERCONFIGA (ANSI)
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
- Wtsapi32.h
api_name:
- WTSUSERCONFIG
- WTSUSERCONFIGA
- WTSUSERCONFIGW
targetos: Windows
req.typenames: WTSUSERCONFIGW, *PWTSUSERCONFIGW
req.redist: 
ms.custom: 19H1
---

# WTSUSERCONFIGW structure


## -description


Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server. This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a> functions.


## -struct-fields




### -field Source

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_source">WTS_CONFIG_SOURCE</a> enumeration type that specifies the  source of configuration information returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a> function.


### -field InheritInitialProgram

A value that indicates whether the client can specify the initial program. This member can be one of the following values.



#### 0

The client cannot specify the initial program. Instead, the program specified by the  <b>InitialProgram</b> member starts automatically when the user logs on to the server. The server logs the user off when the user exits that program.



#### 1

The client can specify the initial program.


### -field AllowLogonTerminalServer

A value that indicates whether the user account is permitted to log on to an RD Session Host server. This member can be one of the following values.



#### 0

The user cannot log on.



#### 1

The user can log on.


### -field TimeoutSettingsConnections

The maximum connection duration, in milliseconds. One minute before the connection expires, the server notifies the user about the pending disconnection. When the connection times out, the server takes the action specified by the  <b>BrokenTimeoutSettings</b> member. Every time the user logs on, the timer is reset. A value of zero indicates that the connection timer is disabled.


### -field TimeoutSettingsDisconnections

The maximum duration, in milliseconds, that the server retains a disconnected session before the logon is terminated. A value of zero indicates that the disconnection timer is disabled.


### -field TimeoutSettingsIdle

The amount of time, in milliseconds, that a connection can remain idle. If there is no keyboard or mouse activity for this period of time, the server takes the action specified by the <b>BrokenTimeoutSettings</b> member. A value of zero indicates that the idle timer is disabled.


### -field DeviceClientDrives

This member is reserved.


### -field DeviceClientPrinters

A value that indicates whether the server automatically connects to previously mapped client printers  when the user logs on to the server. This member can be one of the following values.



#### 0

The server does not automatically connect to previously mapped client printers.



#### 1

The server automatically connects to previously mapped client printers.


### -field ClientDefaultPrinter

A value that indicates whether the client printer is the default printer. This member can be one of the following values.



#### 0

The client printer is not the default printer.



#### 1

The client printer is the default printer.


### -field BrokenTimeoutSettings

The action the server takes when the connection or idle timers expire, or when a connection is lost due to a connection error. This member can be one of the following values.



#### 0

The session is disconnected, but it remains on the server.



#### 1

The session is terminated.


### -field ReconnectSettings

A value that indicates how a disconnected session for this user can be reconnected. This member can be one of the following values.



#### 0

The user can log on to any client computer to reconnect to a disconnected session.



#### 1

The user must log on to the client computer originally used to establish the disconnected session. If the user logs on to a different client computer, the user gets a new session.


### -field ShadowingSettings

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


### -field TerminalServerRemoteHomeDir

A value that indicates whether the <b>TerminalServerHomeDir</b> member contains a path to a local directory or a network share. You cannot set this member by using the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a> function. This member can be one of the following values.



#### 0

The <b>TerminalServerHomeDir</b> member contains a path to a local directory.



#### 1

The <b>TerminalServerHomeDir</b> member contains a path to a network share, and the <b>TerminalServerHomeDirDrive</b> member contains a drive letter to which this path is mapped.


### -field InitialProgram

A null-terminated string that contains the name of  the program to start immediately after the user logs on to the server.


### -field WorkDirectory

A null-terminated string that contains the path of the working directory for the initial program.


### -field TerminalServerProfilePath

A null-terminated string that contains the profile path that is assigned to the user when the user connects to the server. The directory specified by the path must be created manually, and must exist prior to the logon.


### -field TerminalServerHomeDir

A null-terminated string that contains the path to the home folder of the user's Remote Desktop Services sessions. The folder can be a local folder or a network share.


### -field TerminalServerHomeDirDrive

A null-terminated string that contains the drive name (a drive letter followed by a colon) to which the path specified in the <b>TerminalServerHomeDir</b> member is mapped. This member is only valid when the <b>TerminalServerRemoteHomeDir</b> member is set to one.


##### - AllowLogonTerminalServer.0

The user cannot log on.


##### - AllowLogonTerminalServer.1

The user can log on.


##### - BrokenTimeoutSettings.0

The session is disconnected, but it remains on the server.


##### - BrokenTimeoutSettings.1

The session is terminated.


##### - ClientDefaultPrinter.0

The client printer is not the default printer.


##### - ClientDefaultPrinter.1

The client printer is the default printer.


##### - DeviceClientPrinters.0

The server does not automatically connect to previously mapped client printers.


##### - DeviceClientPrinters.1

The server automatically connects to previously mapped client printers.


##### - InheritInitialProgram.0

The client cannot specify the initial program. Instead, the program specified by the  <b>InitialProgram</b> member starts automatically when the user logs on to the server. The server logs the user off when the user exits that program.


##### - InheritInitialProgram.1

The client can specify the initial program.


##### - ReconnectSettings.0

The user can log on to any client computer to reconnect to a disconnected session.


##### - ReconnectSettings.1

The user must log on to the client computer originally used to establish the disconnected session. If the user logs on to a different client computer, the user gets a new session.


##### - ShadowingSettings.0

Remote control is disabled.


##### - ShadowingSettings.1

The user of remote control has full control of the user's session, with the user's permission.


##### - ShadowingSettings.2

The user of remote control has full control of the user's session; the user's permission is 
        not required.


##### - ShadowingSettings.3

The user of remote control can view the session remotely, with the user's permission; the remote user 
        cannot actively control the session.


##### - ShadowingSettings.4

The user of remote control can view the session remotely but not actively control the session; the 
        user's permission is not required.


##### - TerminalServerRemoteHomeDir.0

The <b>TerminalServerHomeDir</b> member contains a path to a local directory.


##### - TerminalServerRemoteHomeDir.1

The <b>TerminalServerHomeDir</b> member contains a path to a network share, and the <b>TerminalServerHomeDirDrive</b> member contains a drive letter to which this path is mapped.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_source">WTS_CONFIG_SOURCE</a>
 

 

