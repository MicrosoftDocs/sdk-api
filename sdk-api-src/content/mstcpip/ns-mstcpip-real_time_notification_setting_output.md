---
UID: NS:mstcpip._REAL_TIME_NOTIFICATION_SETTING_OUTPUT
title: REAL_TIME_NOTIFICATION_SETTING_OUTPUT (mstcpip.h)
description: Provides the output settings from a query for the REAL_TIME_NOTIFICATION_CAPABILITY transport setting for a TCP socket that is used with ControlChannelTrigger to receive background network notifications in a Windows Store app.
helpviewer_keywords: ["*PREAL_TIME_NOTIFICATION_SETTING_OUTPUT","PREAL_TIME_NOTIFICATION_SETTING_OUTPUT","PREAL_TIME_NOTIFICATION_SETTING_OUTPUT structure pointer [Winsock]","REAL_TIME_NOTIFICATION_SETTING_OUTPUT","REAL_TIME_NOTIFICATION_SETTING_OUTPUT structure [Winsock]","mstcpip/PREAL_TIME_NOTIFICATION_SETTING_OUTPUT","mstcpip/REAL_TIME_NOTIFICATION_SETTING_OUTPUT","winsock.real_time_notification_setting_output"]
old-location: winsock\real_time_notification_setting_output.htm
tech.root: WinSock
ms.assetid: 7585CA60-8C7B-4187-A311-72DFA38EB577
ms.date: 12/05/2018
ms.keywords: '*PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, PREAL_TIME_NOTIFICATION_SETTING_OUTPUT structure pointer [Winsock], REAL_TIME_NOTIFICATION_SETTING_OUTPUT, REAL_TIME_NOTIFICATION_SETTING_OUTPUT structure [Winsock], mstcpip/PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, mstcpip/REAL_TIME_NOTIFICATION_SETTING_OUTPUT, winsock.real_time_notification_setting_output'
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
req.typenames: REAL_TIME_NOTIFICATION_SETTING_OUTPUT, *PREAL_TIME_NOTIFICATION_SETTING_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _REAL_TIME_NOTIFICATION_SETTING_OUTPUT
 - mstcpip/_REAL_TIME_NOTIFICATION_SETTING_OUTPUT
 - PREAL_TIME_NOTIFICATION_SETTING_OUTPUT
 - mstcpip/PREAL_TIME_NOTIFICATION_SETTING_OUTPUT
 - REAL_TIME_NOTIFICATION_SETTING_OUTPUT
 - mstcpip/REAL_TIME_NOTIFICATION_SETTING_OUTPUT
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
 - REAL_TIME_NOTIFICATION_SETTING_OUTPUT
---

# REAL_TIME_NOTIFICATION_SETTING_OUTPUT structure


## -description

The <a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_output">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a> structure provides the output settings from a query for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.

## -struct-fields

### -field ChannelStatus

The channel status for a socket that is used with the <a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>.

## -remarks

The <a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_output">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>   structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

 If the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id">TRANSPORT_SETTING_ID</a> in the <i>lpvInBuffer</i> parameter passed to the <a href="/windows/win32/winsock/sio-query-transport-setting">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTL  has the <b>Guid</b> member set to <b>REAL_TIME_NOTIFICATION_CAPABILITY</b>, then this is a request to query the real time notification settings for the TCP socket used with <a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_output">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app. If the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> or <a href="/previous-versions/windows/hardware/network/ff566296(v=vs.85)">LPWSPIoctl</a> call is successful, this IOCTL returns a <a href="/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_input">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a> structure with the current status.

## -see-also

<a href="/windows/desktop/api/mswsock/ne-mswsock-rio_notification_completion_type">CONTROL_CHANNEL_TRIGGER_STATUS</a>



<a href="/uwp/api/windows.networking.sockets.controlchanneltrigger">ControlChannelTrigger</a>



<a href="/windows/win32/api/mstcpip/ns-mstcpip-real_time_notification_setting_input">REAL_TIME_NOTIFICATION_SETTING_INPUT</a>



<a href="/windows/win32/winsock/sio-apply-transport-setting">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="/windows/win32/winsock/sio-query-transport-setting">SIO_QUERY_TRANSPORT_SETTING</a>