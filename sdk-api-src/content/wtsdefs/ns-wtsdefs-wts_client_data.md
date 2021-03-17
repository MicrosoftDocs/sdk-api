---
UID: NS:wtsdefs._WTS_CLIENT_DATA
title: WTS_CLIENT_DATA (wtsdefs.h)
description: Contains information about the client connection.
helpviewer_keywords: ["*PWTS_CLIENT_DATA","PWRDS_CLIENT_DATA","PWRDS_CLIENT_DATA structure pointer [Remote Desktop Services]","PWTS_CLIENT_DATA","PWTS_CLIENT_DATA structure pointer [Remote Desktop Services]","WRDS_CLIENT_DATA","WRDS_CLIENT_DATA structure [Remote Desktop Services]","WTS_CLIENT_DATA","WTS_CLIENT_DATA structure [Remote Desktop Services]","termserv.wts_client_data","wtsdefs/PWRDS_CLIENT_DATA","wtsdefs/PWTS_CLIENT_DATA","wtsdefs/WRDS_CLIENT_DATA","wtsdefs/WTS_CLIENT_DATA"]
old-location: termserv\wts_client_data.htm
tech.root: TermServ
ms.assetid: a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0
ms.date: 12/05/2018
ms.keywords: '*PWTS_CLIENT_DATA, PWRDS_CLIENT_DATA, PWRDS_CLIENT_DATA structure pointer [Remote Desktop Services], PWTS_CLIENT_DATA, PWTS_CLIENT_DATA structure pointer [Remote Desktop Services], WRDS_CLIENT_DATA, WRDS_CLIENT_DATA structure [Remote Desktop Services], WTS_CLIENT_DATA, WTS_CLIENT_DATA structure [Remote Desktop Services], termserv.wts_client_data, wtsdefs/PWRDS_CLIENT_DATA, wtsdefs/PWTS_CLIENT_DATA, wtsdefs/WRDS_CLIENT_DATA, wtsdefs/WTS_CLIENT_DATA'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_CLIENT_DATA, *PWTS_CLIENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CLIENT_DATA
 - wtsdefs/_WTS_CLIENT_DATA
 - PWTS_CLIENT_DATA
 - wtsdefs/PWTS_CLIENT_DATA
 - WTS_CLIENT_DATA
 - wtsdefs/WTS_CLIENT_DATA
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
 - WTS_CLIENT_DATA
---

# WTS_CLIENT_DATA structure


## -description

Contains information about the client connection.

## -struct-fields

### -field fDisableCtrlAltDel

Specifies whether the logon (CTRL+ALT+DELETE) key sequence is disabled.

### -field fDoubleClickDetect

Specifies whether the client can double-click.

### -field fEnableWindowsKey

Specifies whether the Windows key is enabled.

### -field fHideTitleBar

Specifies whether the title bar is hidden.

### -field fInheritAutoLogon

Specifies whether the logon process is automatic. This value overwrites the  <b>fInheritAutoLogon</b> listener registry value.

### -field fPromptForPassword

Specifies whether to prompt the user for a password. If this value is <b>TRUE</b>, the user will be prompted even if the <b>fInheritAutoLogon</b> registry value is <b>TRUE</b> and the "Always ask for a password" policy is not set.

### -field fUsingSavedCreds

Specifies whether the client is using saved credentials during the logon process.

### -field Domain

A string value that specifies the domain of the user. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field UserName

A string value that specifies the user name. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field Password

A string value that specifies the user password. This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field fPasswordIsScPin

Specifies that a smart card was used during the logon process. The smart card PIN is the password.  This value is used if <b>fInheritAutoLogon</b> is set to <b>TRUE</b>.

### -field fInheritInitialProgram

Specifies whether the initial program to start in the Remote Desktop Services shell is inherited. This value overwrites the  <b>fInheritInitialProgram</b> listener registry value.

### -field WorkDirectory

A string value that specifies the directory where the initial program resides. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field InitialProgram

A string value that specifies the name of  the initial program. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field fMaximizeShell

Specifies whether the initial program is displayed maximized. This value is used if <b>fInheritInitialProgram</b> is set to <b>TRUE</b>.

### -field EncryptionLevel

Specifies the encryption level.

### -field PerformanceFlags

Specifies a list of features that can be disabled to increase performance.

### -field ProtocolName

A string value that contains the protocol name.

### -field ProtocolType

Specifies the protocol type.

### -field fInheritColorDepth

Specifies whether to inherit the monitor color depth. This value overwrites the  <b>fInheritColorDepth</b> listener registry value.

### -field HRes

Specifies the client monitor horizontal resolution.

### -field VRes

Specifies the client monitor vertical resolution.

### -field ColorDepth

Specifies the client monitor color depth. For possible values, see the <b>ColorDepth</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a> structure.

### -field DisplayDriverName

A string value that specifies the name of the display driver to load.

### -field DisplayDeviceName

A string value that specifies the name of the display device. For example, if a protocol creates a display device with the name "\\Device\VideoDev0", this field must contain the string "VideoDev".

### -field fMouse

Specifies whether mouse input is enabled.

### -field KeyboardLayout

Specifies the keyboard layout.

### -field KeyboardType

Specifies the keyboard type.

### -field KeyboardSubType

Specifies the keyboard subtype.

### -field KeyboardFunctionKey

Specifies the function key.

### -field imeFileName

Specifies the input method editor name.

### -field ActiveInputLocale

Specifies the input locale identifier. The low word contains a language identifier and the high word contains a device handle to the physical layout of the keyboard.

### -field fNoAudioPlayback

Specifies whether to turn on audio. A value of <b>TRUE</b> specifies no audio.

### -field fRemoteConsoleAudio

Specifies whether to leave audio playback on the remote computer.

### -field AudioDriverName

A string value that contains the name of the audio driver to load.

### -field ClientTimeZone

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_time_zone_information">WTS_TIME_ZONE_INFORMATION</a> structure that contains client time zone information.

### -field ClientName

A string value that contains the fully qualified name of the client computer.

### -field SerialNumber

Client computer serial number.

### -field ClientAddressFamily

The client IP address  family.

### -field ClientAddress

A string value that contains the client IP address in dotted decimal format.

### -field ClientSockAddress

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_sockaddr">WTS_SOCKADDR</a> structure that contains information about the client socket.

### -field ClientDirectory

A string value that contains the client directory.

### -field ClientBuildNumber

Client build number.

### -field ClientProductId

Client product ID.

### -field OutBufCountHost

Number of output buffers on the host computer.

### -field OutBufCountClient

Number of output buffers on the client computer.

### -field OutBufLength

Output buffer length.

### -field ClientSessionId

Client session ID.

### -field ClientDigProductId

A string value that contains a client product identifier.

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

### -field fDisablePNP

Specifies whether PNP redirection is enabled. This value is initially set from policy information. If you reset the value, the policy will be overwritten.