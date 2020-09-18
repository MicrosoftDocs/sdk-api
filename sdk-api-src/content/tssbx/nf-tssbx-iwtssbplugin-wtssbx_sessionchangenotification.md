---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_SessionChangeNotification
title: IWTSSBPlugin::WTSSBX_SessionChangeNotification (tssbx.h)
description: Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in the session.
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","WTSSBX_SessionChangeNotification method","IWTSSBPlugin.WTSSBX_SessionChangeNotification","IWTSSBPlugin::WTSSBX_SessionChangeNotification","WTSSBX_SessionChangeNotification","WTSSBX_SessionChangeNotification method [Remote Desktop Services]","WTSSBX_SessionChangeNotification method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_wtssbx_sessionchangenotification","tssbx/IWTSSBPlugin::WTSSBX_SessionChangeNotification"]
old-location: termserv\iwtssbplugin_wtssbx_sessionchangenotification.htm
tech.root: TermServ
ms.assetid: 00426aa2-1d22-462f-9ad1-2a63d151493d
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_SessionChangeNotification method, IWTSSBPlugin.WTSSBX_SessionChangeNotification, IWTSSBPlugin::WTSSBX_SessionChangeNotification, WTSSBX_SessionChangeNotification, WTSSBX_SessionChangeNotification method [Remote Desktop Services], WTSSBX_SessionChangeNotification method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_sessionchangenotification, tssbx/IWTSSBPlugin::WTSSBX_SessionChangeNotification
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSSBPlugin::WTSSBX_SessionChangeNotification
 - tssbx/IWTSSBPlugin::WTSSBX_SessionChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin.WTSSBX_SessionChangeNotification
---

# IWTSSBPlugin::WTSSBX_SessionChangeNotification


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in the session.

## -parameters

### -param NotificationType [in]

A <a href="/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type">WTSSBX_NOTIFICATION_TYPE</a> type that specifies the type of change that occurred.

### -param MachineId [in]

The ID of the server on which the session change occurred.

### -param NumOfSessions [in]

The number of elements in the <i>SessionInfo</i> array.

### -param SessionInfo [in]

An array of <a href="/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info">WTSSBX_SESSION_INFO</a> structures that contain information about sessions. Only the members that have changed are reported in this structure. The others are set to zero.

## -returns

Returns <b>S_OK</b> if successful.

## -remarks

The <b>WTSSBX_SessionChangeNotification</b> method can report up to 25 sessions each time it is called. If Terminal Services Session Broker (TS Session Broker) needs to report more than 25 sessions, it calls this method multiple times until it reports all of its sessions.

Your implementation of this method must return <b>S_OK</b> immediately if successful.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>