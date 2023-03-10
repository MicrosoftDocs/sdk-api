---
UID: NS:wtsdefs._WRDS_SETTINGS_1
title: WRDS_SETTINGS_1 (wtsdefs.h)
description: Contains policy-related settings for a remote session.
helpviewer_keywords: ["*PWRDS_SETTINGS_1","PWRDS_SETTINGS_1","PWRDS_SETTINGS_1 structure pointer [Remote Desktop Services]","WRDS_SETTINGS_1","WRDS_SETTINGS_1 structure [Remote Desktop Services]","termserv.wrds_settings_1","wtsdefs/PWRDS_SETTINGS_1","wtsdefs/WRDS_SETTINGS_1"]
old-location: termserv\wrds_settings_1.htm
tech.root: TermServ
ms.assetid: 47100A84-49F4-4FF1-8CCB-731638F27C4F
ms.date: 12/05/2018
ms.keywords: '*PWRDS_SETTINGS_1, PWRDS_SETTINGS_1, PWRDS_SETTINGS_1 structure pointer [Remote Desktop Services], WRDS_SETTINGS_1, WRDS_SETTINGS_1 structure [Remote Desktop Services], termserv.wrds_settings_1, wtsdefs/PWRDS_SETTINGS_1, wtsdefs/WRDS_SETTINGS_1'
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
req.typenames: WRDS_SETTINGS_1, *PWRDS_SETTINGS_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_SETTINGS_1
 - wtsdefs/_WRDS_SETTINGS_1
 - PWRDS_SETTINGS_1
 - wtsdefs/PWRDS_SETTINGS_1
 - WRDS_SETTINGS_1
 - wtsdefs/WRDS_SETTINGS_1
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
 - WRDS_SETTINGS_1
---

# WRDS_SETTINGS_1 structure


## -description

Contains policy-related settings for a remote session.

This structure is mostly a subset of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings_1">WRDS_CONNECTION_SETTINGS_1</a> structure. The settings correspond to policy settings that can be found in the group policy editor (Gpedit.exe). The settings in this structure overwrite the initial policy settings.

## -struct-fields

### -field WRdsDisableClipStatus

The clipboard redirection state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791794(v=ws.10)">Device and Resource Redirection</a>.

### -field WRdsDisableClipValue

The clipboard redirection value. A value of 1 indicates that clipboard functionality is disabled (clipboard redirection is enabled); any other value means clipboard functionality is enabled. This value only takes effect if the <b>WRdsDisableClipStatus</b> member is set to enabled.

### -field WRdsDisableLPTStatus

The LPT printer redirection state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791794(v=ws.10)">Device and Resource Redirection</a>.

### -field WRdsDisableLPTValue

The LPT printer redirection value. A value of 1 indicates that LPT printer redirection is enabled; any other value means LPT printer redirection is disabled. This value only takes effect if the <b>WRdsDisableLPTStatus</b> member is set to enabled.

### -field WRdsDisableCcmStatus

The COM port mapping state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791794(v=ws.10)">Device and Resource Redirection</a>.

### -field WRdsDisableCcmValue

The COM port mapping value. A value of 1 indicates that COM port mapping is enabled; any other value means COM port mapping is disabled. This value only takes effect if the <b>WRdsDisableCcmStatus</b> member is set to enabled.

### -field WRdsDisableCdmStatus

The drive mapping state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791794(v=ws.10)">Device and Resource Redirection</a>.

### -field WRdsDisableCdmValue

The drive mapping value. A value of 1 indicates that drive mapping is enabled; any other value means drive mapping is disabled. This value only takes effect if the <b>WRdsDisableCdmStatus</b> member is set to enabled.

### -field WRdsDisableCpmStatus

The printer mapping state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791784(v=ws.10)">Printer Redirection</a>.

### -field WRdsDisableCpmValue

The printer mapping value. A value of 1 indicates that printer mapping is enabled; any other value means printer mapping is disabled. This value only takes effect if the <b>WRdsDisableCpmStatus</b> member is set to enabled.

### -field WRdsDisablePnpStatus

The state of the setting that controls Plug and Play (PNP) redirection (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791794(v=ws.10)">Device and Resource Redirection</a>.

### -field WRdsDisablePnpValue

The PNP redirection value. A value of 1 indicates that PNP redirection is enabled; any other value means PNP redirection is disabled. This value only takes effect if the <b>WRdsDisablePnpStatus</b> member is set to enabled.

### -field WRdsEncryptionLevelStatus

The encryption level state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791904(v=ws.10)">Security</a>.

### -field WRdsEncryptionValue

The encryption level value. This value only takes effect if the <b>WRdsEncryptionLevelStatus</b> member is set to enabled.

### -field WRdsColorDepthStatus

The color depth state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791847(v=ws.10)">Remote Session Environment</a>.

### -field WRdsColorDepthValue

The color depth value. For possible values, see the <b>ColorDepth</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a> structure. This value only takes effect if the <b>WRdsColorDepthStatus</b> member is set to enabled.

### -field WRdsDisableAutoReconnecetStatus

The automatic client reconnection state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791922(v=ws.10)">Connections</a>.

### -field WRdsDisableAutoReconnecetValue

The automatic client reconnection value. A value of 1 indicates that automatic client reconnection is disabled; any other value means automatic client reconnection is enabled. This value only takes effect if the <b>WRdsDisableAutoReconnecetStatus</b> member is set to enabled.

### -field WRdsDisableEncryptionStatus

The state (not applicable, disabled, enabled, or not configured) of the setting that controls whether to disable encryption for communication between the client and the server. For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791904(v=ws.10)">Security</a>.

### -field WRdsDisableEncryptionValue

The encryption disabling value. A value of 1 indicates that encryption is disabled; any other value means encryption is required. This value only takes effect if the <b>WRdsDisableEncryptionStatus</b> member is set to enabled.

### -field WRdsResetBrokenStatus

The state (not applicable, disabled, enabled, or not configured) of the setting that controls how the server reacts when the connection or idle timers expire, or when a connection is lost due to a connection error. For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791741(v=ws.10)">Session Time Limits</a>.

### -field WRdsResetBrokenValue

The value of the setting that controls the server reaction.  A value of 1 indicates that the session is terminated whenever the time-out limit is reached; any other value means the session is disconnected but remains on the server. This value only takes effect if the <b>WRdsResetBrokenStatus</b> member is set to enabled.

### -field WRdsMaxIdleTimeStatus

The maximum idle time state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791741(v=ws.10)">Session Time Limits</a>.

### -field WRdsMaxIdleTimeValue

The maximum amount of time, in minutes, that the Remote Desktop Services session can remain idle. This value only takes effect if the <b>WRdsMaxIdleTimeStatus</b> member is set to enabled.

### -field WRdsMaxDisconnectTimeStatus

The maximum disconnection time state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791741(v=ws.10)">Session Time Limits</a>.

### -field WRdsMaxDisconnectTimeValue

The maximum amount of time, in minutes, that a disconnected Remote Desktop Services session remains active on the RD Session Host server.

This value only takes effect if the <b>WRdsMaxDisconnectTimeStatus</b> member is set to enabled.

### -field WRdsMaxConnectTimeStatus

The maximum connection time state (not applicable, disabled, enabled, or not configured). For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791741(v=ws.10)">Session Time Limits</a>.

### -field WRdsMaxConnectTimeValue

The maximum duration of the Remote Desktop Services session, in minutes. This value only takes effect if the <b>WRdsMaxConnectTimeStatus</b> member is set to enabled.

### -field WRdsKeepAliveStatus

The state (not applicable, disabled, enabled, or not configured) of the <i>keep alive</i> setting.  The keep alive setting controls whether to check to keep a Remote Desktop Services session active. For more information, see the group policy node topic for <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791922(v=ws.10)">Connections</a>.

### -field WRdsKeepAliveStartValue

Specifies whether or not the keep alive setting is enabled.



#### TRUE

The keep alive setting is enabled.



#### FALSE

The keep alive setting is disabled.

### -field WRdsKeepAliveIntervalValue

The amount of time, in minutes, of idle time before the state of the Remote Desktop Services session is checked. This value only takes effect if the <b>WRdsKeepAliveStatus</b> member is set to enabled.

## -see-also

<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee791760(v=ws.10)">Remote Desktop Session Host</a>