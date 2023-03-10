---
UID: NS:wtsdefs._WRDS_CONNECTION_SETTINGS_1
title: WRDS_CONNECTION_SETTINGS_1 (wtsdefs.h)
description: Contains connection setting information for a remote session. (WRDS_CONNECTION_SETTINGS_1)
helpviewer_keywords: ["*PWRDS_CONNECTION_SETTINGS_1","PWRDS_CONNECTION_SETTINGS_1","PWRDS_CONNECTION_SETTINGS_1 structure pointer [Remote Desktop Services]","WRDS_CONNECTION_SETTINGS_1","WRDS_CONNECTION_SETTINGS_1 structure [Remote Desktop Services]","WRDS_PERF_DISABLE_CURSORSETTINGS","WRDS_PERF_DISABLE_CURSOR_SHADOW","WRDS_PERF_DISABLE_FULLWINDOWDRAG","WRDS_PERF_DISABLE_MENUANIMATIONS","WRDS_PERF_DISABLE_NOTHING","WRDS_PERF_DISABLE_THEMING","WRDS_PERF_DISABLE_WALLPAPER","WRDS_PERF_ENABLE_DESKTOP_COMPOSITION","WRDS_PERF_ENABLE_ENHANCED_GRAPHICS","WRDS_PERF_ENABLE_FONT_SMOOTHING","termserv.wrds_connection_settings_1","wtsdefs/PWRDS_CONNECTION_SETTINGS_1","wtsdefs/WRDS_CONNECTION_SETTINGS_1"]
old-location: termserv\wrds_connection_settings_1.htm
tech.root: TermServ
ms.assetid: 93D4C843-7974-4287-9222-B90206DE6B75
ms.date: 12/05/2018
ms.keywords: '*PWRDS_CONNECTION_SETTINGS_1, PWRDS_CONNECTION_SETTINGS_1, PWRDS_CONNECTION_SETTINGS_1 structure pointer [Remote Desktop Services], WRDS_CONNECTION_SETTINGS_1, WRDS_CONNECTION_SETTINGS_1 structure [Remote Desktop Services], WRDS_PERF_DISABLE_CURSORSETTINGS, WRDS_PERF_DISABLE_CURSOR_SHADOW, WRDS_PERF_DISABLE_FULLWINDOWDRAG, WRDS_PERF_DISABLE_MENUANIMATIONS, WRDS_PERF_DISABLE_NOTHING, WRDS_PERF_DISABLE_THEMING, WRDS_PERF_DISABLE_WALLPAPER, WRDS_PERF_ENABLE_DESKTOP_COMPOSITION, WRDS_PERF_ENABLE_ENHANCED_GRAPHICS, WRDS_PERF_ENABLE_FONT_SMOOTHING, termserv.wrds_connection_settings_1, wtsdefs/PWRDS_CONNECTION_SETTINGS_1, wtsdefs/WRDS_CONNECTION_SETTINGS_1'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WRDS_CONNECTION_SETTINGS_1, *PWRDS_CONNECTION_SETTINGS_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_CONNECTION_SETTINGS_1
 - wtsdefs/_WRDS_CONNECTION_SETTINGS_1
 - PWRDS_CONNECTION_SETTINGS_1
 - wtsdefs/PWRDS_CONNECTION_SETTINGS_1
 - WRDS_CONNECTION_SETTINGS_1
 - wtsdefs/WRDS_CONNECTION_SETTINGS_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WRDS_CONNECTION_SETTINGS_1
---

# WRDS_CONNECTION_SETTINGS_1 structure


## -description

Contains connection setting information for a remote session.

## -struct-fields

### -field fInheritInitialProgram

Specifies whether the initial program to start in the Remote Desktop Services shell is inherited. This value overwrites the  <b>fInheritInitialProgram</b> listener registry value.

### -field fInheritColorDepth

Specifies whether to inherit the monitor color depth. This value overwrites the  <b>fInheritColorDepth</b> listener registry value.

### -field fHideTitleBar

Specifies whether the title bar is hidden.

### -field fInheritAutoLogon

Specifies whether the logon process is automatic. This value overwrites the  <b>fInheritAutoLogon</b> listener registry value.

### -field fMaximizeShell

Specifies whether the initial program is displayed maximized. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field fDisablePNP

Specifies whether PNP redirection is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fPasswordIsScPin

Specifies that a smart card was used during the logon process. The smart card PIN is the password.  This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field fPromptForPassword

Specifies whether to prompt the user for a password. If this value is <b>TRUE</b>, the user will be prompted even if the <b>fInheritAutoLogon</b> registry value is <b>TRUE</b> and the "Always ask for a password" policy is not set.

### -field fDisableCpm

Specifies whether printer mapping is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fDisableCdm

Specifies whether drive mapping is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fDisableCcm

Specifies whether COM port  mapping is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fDisableLPT

Specifies whether LPT printer redirection is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fDisableClip

Specifies whether clipboard redirection is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.

### -field fResetBroken

Specifies the action the server takes when the connection or idle timers expire, or when a connection is lost due to a connection error.



#### FALSE

The session is disconnected, but it remains on the server.



#### TRUE

The session is terminated.

### -field fDisableEncryption

Specifies whether to disable encryption for communication between the client and server.

### -field fDisableAutoReconnect

Specifies whether to disable automatic reconnect of the client.

### -field fDisableCtrlAltDel

Specifies whether the Ctrl+Alt+Delete keyboard shortcut is disabled.

### -field fDoubleClickDetect

Specifies whether the client can double-click.

### -field fEnableWindowsKey

Specifies whether the Windows key is enabled.

### -field fUsingSavedCreds

Specifies whether the client is using saved credentials during the logon process.

### -field fMouse

Specifies whether mouse input is enabled.

### -field fNoAudioPlayback

Specifies whether to turn on audio playback. A value of <b>TRUE</b> specifies no audio.

### -field fRemoteConsoleAudio

Specifies whether to leave audio playback on the remote computer.

### -field EncryptionLevel

Specifies the encryption level.

### -field ColorDepth

Specifies the client monitor color depth. For possible values, see the <b>ColorDepth</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a> structure.

### -field ProtocolType

Specifies the protocol type.

### -field HRes

Specifies the client monitor horizontal resolution.

### -field VRes

Specifies the client monitor vertical resolution.

### -field ClientProductId

The client software product id.

### -field OutBufCountHost

The number of output buffers on the host.

### -field OutBufCountClient

The number of output buffers on the client.

### -field OutBufLength

The length of output buffers, in bytes.

### -field KeyboardLayout

Specifies the keyboard layout.

### -field MaxConnectionTime

The maximum duration of the Remote Desktop Services session, in minutes.

### -field MaxDisconnectionTime

The maximum amount of time, in minutes, that a disconnected Remote Desktop Services session remains active on the RD Session Host server.

### -field MaxIdleTime

The maximum amount of time, in minutes, that the Remote Desktop Services session can remain idle.

### -field PerformanceFlags

Specifies a set of features that can be set at the server to improve performance. This can be a combination of one or more of the following values.



#### WRDS_PERF_DISABLE_NOTHING (0x00000000)

No features are disabled.



#### WRDS_PERF_DISABLE_WALLPAPER (0x00000001)

Wallpaper on the desktop is not displayed.



#### WRDS_PERF_DISABLE_FULLWINDOWDRAG (0x00000002)

Full-window drag is disabled; only the window outline is displayed when the window is moved.



#### WRDS_PERF_DISABLE_MENUANIMATIONS (0x00000004)

Menu animations are disabled.



#### WRDS_PERF_DISABLE_THEMING (0x00000008)

Themes are disabled.



#### WRDS_PERF_ENABLE_ENHANCED_GRAPHICS (0x00000010)

Enable enhanced graphics.



#### WRDS_PERF_DISABLE_CURSOR_SHADOW (0x00000020)

No shadow is displayed for the cursor.



#### WRDS_PERF_DISABLE_CURSORSETTINGS (0x00000040)

Cursor blinking is disabled.



#### WRDS_PERF_ENABLE_FONT_SMOOTHING (0x00000080)

Enable font smoothing.



#### WRDS_PERF_ENABLE_DESKTOP_COMPOSITION (0x00000100)

Enable desktop composition.

### -field KeyboardType

Specifies the keyboard type.

### -field KeyboardSubType

Specifies the keyboard subtype.

### -field KeyboardFunctionKey

Specifies the function key.

### -field ActiveInputLocale

Specifies the input locale identifier. The low word contains a language identifier and the high word contains a device handle to the physical layout of the keyboard.

### -field SerialNumber

The client computer's unique serial number.

### -field ClientAddressFamily

The client IP address  family.

### -field ClientBuildNumber

The client build number.

### -field ClientSessionId

The client session Id.

### -field WorkDirectory

A string that contains the directory where the initial program resides. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field InitialProgram

A string value that specifies the name of  the initial program. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field UserName

A string that specifies the user name. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field Domain

A string that specifies the domain of the user. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field Password

A string that specifies the user password. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field ProtocolName

A string that contains the protocol name.

### -field DisplayDriverName

A string that specifies the name of the display driver to load.

### -field DisplayDeviceName

A string that specifies the name of the display device.

### -field imeFileName

Specifies the input method editor name.

### -field AudioDriverName

A string that contains the name of the audio driver to load.

### -field ClientName

A string that contains the fully qualified name of the client computer.

### -field ClientAddress

A string that contains the client IP address in dotted decimal format.

### -field ClientDirectory

The client directory.

A string that contains the client directory.

### -field ClientDigProductId

A string that contains a client product identifier.

### -field ClientSockAddress

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_sockaddr">WRDS_SOCKADDR</a> structure that contains socket address information.

### -field ClientTimeZone

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_time_zone_information">WRDS_TIME_ZONE_INFORMATION</a> structure that contains client time zone information.

### -field WRdsListenerSettings

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_settings">WRDS_LISTENER_SETTINGS</a> structure that contains listener settings.

### -field EventLogActivityId

### -field ContextSize.range

### -field ContextSize.range.0

### -field ContextSize.range.16384

### -field ContextData.size_is

### -field ContextData.size_is.ContextSize

### -field ContextSize

The size, in bytes, of the <b>ContextData</b> array.

### -field ContextData

An array of bytes that contains contextual data for the connection. The size of this array is specified in the <b>ContextSize</b> member.
