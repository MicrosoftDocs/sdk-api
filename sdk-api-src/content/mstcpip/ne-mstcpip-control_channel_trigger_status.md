---
UID: NE:mstcpip.__unnamed_enum_0
title: CONTROL_CHANNEL_TRIGGER_STATUS (mstcpip.h)
description: Specifies the status from a query for the REAL_TIME_NOTIFICATION_CAPABILITY transport setting for a TCP socket that is used with ControlChannelTrigger to receive background network notifications in a Windows Store app.
helpviewer_keywords: ["*PCONTROL_CHANNEL_TRIGGER_STATUS","CONTROL_CHANNEL_TRIGGER_STATUS","CONTROL_CHANNEL_TRIGGER_STATUS enumeration [Winsock]","CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED","CONTROL_CHANNEL_TRIGGER_STATUS_INVALID","CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR","CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE","CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED","CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR","CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_INVALID","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR","mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED","winsock.control_channel_trigger_status"]
old-location: winsock\control_channel_trigger_status.htm
tech.root: WinSock
ms.assetid: D2E7663E-C388-48A5-8553-72DE2213CA97
ms.date: 12/05/2018
ms.keywords: '*PCONTROL_CHANNEL_TRIGGER_STATUS, CONTROL_CHANNEL_TRIGGER_STATUS, CONTROL_CHANNEL_TRIGGER_STATUS enumeration [Winsock], CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED, CONTROL_CHANNEL_TRIGGER_STATUS_INVALID, CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR, CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE, CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED, CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR, CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_INVALID, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED, winsock.control_channel_trigger_status'
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CONTROL_CHANNEL_TRIGGER_STATUS, *PCONTROL_CHANNEL_TRIGGER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCONTROL_CHANNEL_TRIGGER_STATUS
 - mstcpip/PCONTROL_CHANNEL_TRIGGER_STATUS
 - CONTROL_CHANNEL_TRIGGER_STATUS
 - mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - CONTROL_CHANNEL_TRIGGER_STATUS
---

# CONTROL_CHANNEL_TRIGGER_STATUS enumeration


## -description

The <a href="/windows/desktop/api/mswsock/ne-mswsock-rio_notification_completion_type">CONTROL_CHANNEL_TRIGGER_STATUS</a> enumeration specifies the status from a query for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.

## -enum-fields

### -field CONTROL_CHANNEL_TRIGGER_STATUS_INVALID:0

Status is invalid.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED:1

A software slot was allocated for the <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED:2

A hardware slot was allocated for the <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR:3

A status policy error.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR:4

A status system error.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED:5

The TCP transport is disconnected.

### -field CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE:6

Service is unavailable.

## -remarks

The <a href="/windows/desktop/api/mswsock/ne-mswsock-rio_notification_completion_type">CONTROL_CHANNEL_TRIGGER_STATUS</a>  structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

A <a href="/windows/desktop/api/mswsock/ne-mswsock-rio_notification_completion_type">CONTROL_CHANNEL_TRIGGER_STATUS</a> enumeration value is returned as output from the <a href="/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTL to a query the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.

## -see-also

<a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>



<a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_output">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)">SIO_QUERY_TRANSPORT_SETTING</a>
