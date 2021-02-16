---
UID: NE:wtsapi32._WTS_CONFIG_CLASS
title: WTS_CONFIG_CLASS (wtsapi32.h)
description: Contains values that indicate the type of user configuration information to set or retrieve in a call to the WTSQueryUserConfig and WTSSetUserConfig functions.
helpviewer_keywords: ["WTSUserConfigBrokenTimeoutSettings","WTSUserConfigInitialProgram","WTSUserConfigModemCallbackPhoneNumber","WTSUserConfigModemCallbackSettings","WTSUserConfigReconnectSettings","WTSUserConfigShadowingSettings","WTSUserConfigTerminalServerHomeDir","WTSUserConfigTerminalServerHomeDirDrive","WTSUserConfigTerminalServerProfilePath","WTSUserConfigTimeoutSettingsConnections","WTSUserConfigTimeoutSettingsDisconnections","WTSUserConfigTimeoutSettingsIdle","WTSUserConfigUser","WTSUserConfigWorkingDirectory","WTSUserConfigfAllowLogonTerminalServer","WTSUserConfigfDeviceClientDefaultPrinter","WTSUserConfigfDeviceClientDrives","WTSUserConfigfDeviceClientPrinters","WTSUserConfigfInheritInitialProgram","WTSUserConfigfTerminalServerRemoteHomeDir","WTS_CONFIG_CLASS","WTS_CONFIG_CLASS enumeration [Remote Desktop Services]","_win32_wts_config_class_str","termserv.wts_config_class_str","wtsapi32/WTSUserConfigBrokenTimeoutSettings","wtsapi32/WTSUserConfigInitialProgram","wtsapi32/WTSUserConfigModemCallbackPhoneNumber","wtsapi32/WTSUserConfigModemCallbackSettings","wtsapi32/WTSUserConfigReconnectSettings","wtsapi32/WTSUserConfigShadowingSettings","wtsapi32/WTSUserConfigTerminalServerHomeDir","wtsapi32/WTSUserConfigTerminalServerHomeDirDrive","wtsapi32/WTSUserConfigTerminalServerProfilePath","wtsapi32/WTSUserConfigTimeoutSettingsConnections","wtsapi32/WTSUserConfigTimeoutSettingsDisconnections","wtsapi32/WTSUserConfigTimeoutSettingsIdle","wtsapi32/WTSUserConfigUser","wtsapi32/WTSUserConfigWorkingDirectory","wtsapi32/WTSUserConfigfAllowLogonTerminalServer","wtsapi32/WTSUserConfigfDeviceClientDefaultPrinter","wtsapi32/WTSUserConfigfDeviceClientDrives","wtsapi32/WTSUserConfigfDeviceClientPrinters","wtsapi32/WTSUserConfigfInheritInitialProgram","wtsapi32/WTSUserConfigfTerminalServerRemoteHomeDir","wtsapi32/WTS_CONFIG_CLASS"]
old-location: termserv\wts_config_class_str.htm
tech.root: TermServ
ms.assetid: 623b8a86-aa0d-497c-a2e6-5526f9b13d98
ms.date: 12/05/2018
ms.keywords: WTSUserConfigBrokenTimeoutSettings, WTSUserConfigInitialProgram, WTSUserConfigModemCallbackPhoneNumber, WTSUserConfigModemCallbackSettings, WTSUserConfigReconnectSettings, WTSUserConfigShadowingSettings, WTSUserConfigTerminalServerHomeDir, WTSUserConfigTerminalServerHomeDirDrive, WTSUserConfigTerminalServerProfilePath, WTSUserConfigTimeoutSettingsConnections, WTSUserConfigTimeoutSettingsDisconnections, WTSUserConfigTimeoutSettingsIdle, WTSUserConfigUser, WTSUserConfigWorkingDirectory, WTSUserConfigfAllowLogonTerminalServer, WTSUserConfigfDeviceClientDefaultPrinter, WTSUserConfigfDeviceClientDrives, WTSUserConfigfDeviceClientPrinters, WTSUserConfigfInheritInitialProgram, WTSUserConfigfTerminalServerRemoteHomeDir, WTS_CONFIG_CLASS, WTS_CONFIG_CLASS enumeration [Remote Desktop Services], _win32_wts_config_class_str, termserv.wts_config_class_str, wtsapi32/WTSUserConfigBrokenTimeoutSettings, wtsapi32/WTSUserConfigInitialProgram, wtsapi32/WTSUserConfigModemCallbackPhoneNumber, wtsapi32/WTSUserConfigModemCallbackSettings, wtsapi32/WTSUserConfigReconnectSettings, wtsapi32/WTSUserConfigShadowingSettings, wtsapi32/WTSUserConfigTerminalServerHomeDir, wtsapi32/WTSUserConfigTerminalServerHomeDirDrive, wtsapi32/WTSUserConfigTerminalServerProfilePath, wtsapi32/WTSUserConfigTimeoutSettingsConnections, wtsapi32/WTSUserConfigTimeoutSettingsDisconnections, wtsapi32/WTSUserConfigTimeoutSettingsIdle, wtsapi32/WTSUserConfigUser, wtsapi32/WTSUserConfigWorkingDirectory, wtsapi32/WTSUserConfigfAllowLogonTerminalServer, wtsapi32/WTSUserConfigfDeviceClientDefaultPrinter, wtsapi32/WTSUserConfigfDeviceClientDrives, wtsapi32/WTSUserConfigfDeviceClientPrinters, wtsapi32/WTSUserConfigfInheritInitialProgram, wtsapi32/WTSUserConfigfTerminalServerRemoteHomeDir, wtsapi32/WTS_CONFIG_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_CONFIG_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CONFIG_CLASS
 - wtsapi32/_WTS_CONFIG_CLASS
 - WTS_CONFIG_CLASS
 - wtsapi32/WTS_CONFIG_CLASS
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
 - WTS_CONFIG_CLASS
---

# WTS_CONFIG_CLASS enumeration


## -description

Contains 
    values that indicate the type of user configuration information to set or retrieve in a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a> and 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a> functions.

## -enum-fields

### -field WTSUserConfigInitialProgram

A null-terminated string that contains the path of the initial program that Remote Desktop Services runs when the 
      user logs on.

If the <b>WTSUserConfigfInheritInitialProgram</b> value is 1, the initial program can be 
       any program specified by the client.

### -field WTSUserConfigWorkingDirectory

A null-terminated string that contains the path of the working directory for the initial program.

### -field WTSUserConfigfInheritInitialProgram

A value that indicates whether the client can specify the initial program.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The client cannot specify the initial program. Instead, the 
         <b>WTSUserConfigInitialProgram</b> string identifies an initial program that runs 
         automatically when the user logs on to a remote computer. Remote Desktop Services logs the user off when the user 
         exits that program.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The client can specify the initial program.

</td>
</tr>
</table>

### -field WTSUserConfigfAllowLogonTerminalServer

A value that indicates whether the user account is permitted to log on to an RD Session Host server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The user cannot log on.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The user can log on.

</td>
</tr>
</table>

### -field WTSUserConfigTimeoutSettingsConnections

A <b>DWORD</b> value that specifies the maximum connection duration, in milliseconds. 
      One minute before the connection time-out interval expires, the user is notified of the pending disconnection. 
      The user's session is disconnected or terminated depending on the 
      <b>WTSUserConfigBrokenTimeoutSettings</b> value. Every time the user logs on, the timer is 
      reset. A value of zero indicates that the connection timer is disabled.

### -field WTSUserConfigTimeoutSettingsDisconnections

A <b>DWORD</b> value that specifies the maximum duration, in milliseconds, that an 
      RD Session Host server retains a disconnected session before the logon is terminated. A value of zero indicates that the 
      disconnection timer is disabled.

### -field WTSUserConfigTimeoutSettingsIdle

A <b>DWORD</b> value that specifies the maximum idle time, in milliseconds. If there 
      is no keyboard or mouse activity for the specified interval, the user's session is disconnected or terminated 
      depending on the <b>WTSUserConfigBrokenTimeoutSettings</b> value. A value of zero 
      indicates that the idle timer is disabled.

### -field WTSUserConfigfDeviceClientDrives

This constant currently is not used by Remote Desktop Services.

A value that indicates whether the RD Session Host server automatically reestablishes 
      client drive mappings at logon.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The server does not automatically connect to previously mapped client drives.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The server automatically connects to previously mapped client drives at logon.

</td>
</tr>
</table>

### -field WTSUserConfigfDeviceClientPrinters

RDP 5.0 and later clients: A value that indicates whether the RD Session Host server 
      automatically reestablishes client printer mappings at logon.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The server does not automatically connect to previously mapped client printers.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The server automatically connects to previously mapped client printers at logon.

</td>
</tr>
</table>

### -field WTSUserConfigfDeviceClientDefaultPrinter

RDP 5.0 and later clients: A value that indicates whether the client printer 
      is the default printer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The client printer is not the default printer.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The client printer is the default printer.

</td>
</tr>
</table>

### -field WTSUserConfigBrokenTimeoutSettings

A value that indicates what happens when the connection or idle timers expire or when a connection is lost 
      due to a connection error.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The session is disconnected.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The session is terminated.

</td>
</tr>
</table>

### -field WTSUserConfigReconnectSettings

A value that indicates how a disconnected session for this user can be reconnected.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The user can log on to any client computer to reconnect to a disconnected session.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The user can reconnect to a disconnected session by logging on to the client computer used to establish 
         the disconnected session. If the user logs on from a different client computer, the user gets a new logon 
         session.

</td>
</tr>
</table>

### -field WTSUserConfigModemCallbackSettings

This constant currently is not used by Remote Desktop Services.

A value that indicates the configuration for dial-up connections in which the 
      RD Session Host server stops responding and then calls back the client to establish the connection.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
Callback connections are disabled.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The server prompts the user to enter a phone number and calls the user back at that phone number. You can 
         use the <b>WTSUserConfigModemCallbackPhoneNumber</b> value to specify a default phone 
         number.

</td>
</tr>
<tr>
<td>
2

</td>
<td>
The server automatically calls the user back at the phone number specified by the
         <b>WTSUserConfigModemCallbackPhoneNumber</b> value.

</td>
</tr>
</table>

### -field WTSUserConfigModemCallbackPhoneNumber

This constant currently is not used by Remote Desktop Services.

A null-terminated string that contains the phone number to use for callback 
      connections.

### -field WTSUserConfigShadowingSettings

RDP 5.0 and later clients: A value that indicates whether the user session 
      can be shadowed. Shadowing allows a user to remotely monitor the on-screen operations of another user.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
Disable

</td>
</tr>
<tr>
<td>
1

</td>
<td>
Enable input, notify

</td>
</tr>
<tr>
<td>
2

</td>
<td>
Enable input, no notify

</td>
</tr>
<tr>
<td>
3

</td>
<td>
Enable no input, notify

</td>
</tr>
<tr>
<td>
4

</td>
<td>
Enable no input, no notify

</td>
</tr>
</table>

### -field WTSUserConfigTerminalServerProfilePath

A null-terminated string that contains the path of the user's profile for RD Session Host server logon. The directory 
      the path identifies must be created manually, and must exist prior to the logon. 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a> will not create the directory 
      if it does not already exist.

### -field WTSUserConfigTerminalServerHomeDir

A null-terminated string that contains the path of the user's root directory for RD Session Host server logon. This 
      string can specify a local path or a UNC path (<i>\\ComputerName\Share\Path</i>). For more information, see 
      <b>WTSUserConfigfTerminalServerRemoteHomeDir</b>.

### -field WTSUserConfigTerminalServerHomeDirDrive

A null-terminated string that contains a drive name (a drive letter followed by a colon) to which the UNC 
      path specified in the <b>WTSUserConfigTerminalServerHomeDir</b> string is mapped. For more information, see
      <b>WTSUserConfigfTerminalServerRemoteHomeDir</b>.

### -field WTSUserConfigfTerminalServerRemoteHomeDir

A value that indicates whether the user's root directory for RD Session Host server logon is a local path or a 
      mapped drive letter. Note that this value cannot be used with 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The <b>WTSUserConfigTerminalServerHomeDir</b> string contains the local path of the 
         user's RD Session Host server logon root directory.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The <b>WTSUserConfigTerminalServerHomeDir</b> string contains the UNC path of the 
         user's RD Session Host server logon root directory, and the 
         <b>WTSUserConfigTerminalServerHomeDirDrive</b> string contains a drive letter to which 
         the UNC path is mapped.

</td>
</tr>
</table>

### -field WTSUserConfigUser

A <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsuserconfiga">WTSUSERCONFIG</a> structure that contains configuration data for the session. 

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a>