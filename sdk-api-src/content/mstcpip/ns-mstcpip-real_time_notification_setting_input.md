---
UID: NS:mstcpip._REAL_TIME_NOTIFICATION_SETTING_INPUT
title: REAL_TIME_NOTIFICATION_SETTING_INPUT (mstcpip.h)
description: Provides input settings to apply for the REAL_TIME_NOTIFICATION_CAPABILITY transport setting for a TCP socket that is used with ControlChannelTrigger to receive background network notifications in a Windows Store app.
helpviewer_keywords: ["*PREAL_TIME_NOTIFICATION_SETTING_INPUT","PREAL_TIME_NOTIFICATION_SETTING_INPUT","PREAL_TIME_NOTIFICATION_SETTING_INPUT structure pointer [Winsock]","REAL_TIME_NOTIFICATION_SETTING_INPUT","REAL_TIME_NOTIFICATION_SETTING_INPUT structure [Winsock]","mstcpip/PREAL_TIME_NOTIFICATION_SETTING_INPUT","mstcpip/REAL_TIME_NOTIFICATION_SETTING_INPUT","winsock.real_time_notification_setting_input"]
old-location: winsock\real_time_notification_setting_input.htm
tech.root: WinSock
ms.assetid: A008310D-D812-4DCD-A3F2-64FEEEB31DB8
ms.date: 12/05/2018
ms.keywords: '*PREAL_TIME_NOTIFICATION_SETTING_INPUT, PREAL_TIME_NOTIFICATION_SETTING_INPUT, PREAL_TIME_NOTIFICATION_SETTING_INPUT structure pointer [Winsock], REAL_TIME_NOTIFICATION_SETTING_INPUT, REAL_TIME_NOTIFICATION_SETTING_INPUT structure [Winsock], mstcpip/PREAL_TIME_NOTIFICATION_SETTING_INPUT, mstcpip/REAL_TIME_NOTIFICATION_SETTING_INPUT, winsock.real_time_notification_setting_input'
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
req.typenames: REAL_TIME_NOTIFICATION_SETTING_INPUT, *PREAL_TIME_NOTIFICATION_SETTING_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _REAL_TIME_NOTIFICATION_SETTING_INPUT
 - mstcpip/_REAL_TIME_NOTIFICATION_SETTING_INPUT
 - PREAL_TIME_NOTIFICATION_SETTING_INPUT
 - mstcpip/PREAL_TIME_NOTIFICATION_SETTING_INPUT
 - REAL_TIME_NOTIFICATION_SETTING_INPUT
 - mstcpip/REAL_TIME_NOTIFICATION_SETTING_INPUT
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
 - REAL_TIME_NOTIFICATION_SETTING_INPUT
---

# REAL_TIME_NOTIFICATION_SETTING_INPUT structure


## -description

The <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b> structure provides input settings to apply for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.

## -struct-fields

### -field TransportSettingId

The transport setting ID.

### -field BrokerEventGuid

The realtime notification broker event GUID for this transport ID.

## -remarks

The <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b>  structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

 If the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id">TRANSPORT_SETTING_ID</a> in the <i>lpvInBuffer</i> parameter passed to the <a href="/windows/win32/winsock/sio-apply-transport-setting">SIO_APPLY_TRANSPORT_SETTING</a> 
        IOCTL  has the <b>Guid</b> member set to <b>REAL_TIME_NOTIFICATION_CAPABILITY</b>, then this is a request to query the real time notification settings for the TCP socket used with <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app. The <i>lpvInBuffer</i> parameter should point to a <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b> structure used as input to the <b>SIO_APPLY_TRANSPORT_SETTING</b> 
        IOCTL to apply the transport setting.

## -see-also

<a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>



<a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_output">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="/windows/win32/winsock/sio-apply-transport-setting">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="/windows/win32/winsock/sio-query-transport-setting">SIO_QUERY_TRANSPORT_SETTING</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id">TRANSPORT_SETTING_ID</a>