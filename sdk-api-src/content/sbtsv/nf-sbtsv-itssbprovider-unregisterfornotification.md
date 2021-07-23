---
UID: NF:sbtsv.ITsSbProvider.UnRegisterForNotification
title: ITsSbProvider::UnRegisterForNotification (sbtsv.h)
description: Requests that Remote Desktop Connection Broker (RD Connection Broker) not send notifications about specified events.
helpviewer_keywords: ["ITsSbProvider interface [Remote Desktop Services]","UnRegisterForNotification method","ITsSbProvider.UnRegisterForNotification","ITsSbProvider::UnRegisterForNotification","TSSB_NOTIFY_CONNECTION_REQUEST_CHANGE","TSSB_NOTIFY_SESSION_CHANGE","TSSB_NOTIFY_TARGET_CHANGE","UnRegisterForNotification","UnRegisterForNotification method [Remote Desktop Services]","UnRegisterForNotification method [Remote Desktop Services]","ITsSbProvider interface","sbtsv/ITsSbProvider::UnRegisterForNotification","termserv.itssbprovider_unregisterfornotification"]
old-location: termserv\itssbprovider_unregisterfornotification.htm
tech.root: TermServ
ms.assetid: e2fa297e-9923-4e60-9e6e-caa6e4b8c963
ms.date: 12/05/2018
ms.keywords: ITsSbProvider interface [Remote Desktop Services],UnRegisterForNotification method, ITsSbProvider.UnRegisterForNotification, ITsSbProvider::UnRegisterForNotification, TSSB_NOTIFY_CONNECTION_REQUEST_CHANGE, TSSB_NOTIFY_SESSION_CHANGE, TSSB_NOTIFY_TARGET_CHANGE, UnRegisterForNotification, UnRegisterForNotification method [Remote Desktop Services], UnRegisterForNotification method [Remote Desktop Services],ITsSbProvider interface, sbtsv/ITsSbProvider::UnRegisterForNotification, termserv.itssbprovider_unregisterfornotification
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbProvider::UnRegisterForNotification
 - sbtsv/ITsSbProvider::UnRegisterForNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.UnRegisterForNotification
---

# ITsSbProvider::UnRegisterForNotification


## -description

Requests that  Remote Desktop Connection Broker (RD Connection Broker) not send notifications about specified events.

## -parameters

### -param notificationType [in]

Specifies the type of notification. To specify more than one type, use a logical <b>OR</b>.



#### TSSB_NOTIFY_TARGET_CHANGE

The owner plug-in has recognized a change in the change in the target's state.



#### TSSB_NOTIFY_SESSION_CHANGE

The owner plug-in has recognized a change in the change in the session's state.



#### TSSB_NOTIFY_CONNECTION_REQUEST_CHANGE

RD Connection Broker has created a connection, or completed a connection request due to a successful logon, time-out, or connection failure.

### -param ResourceToMonitor [in]

This parameter is reserved.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins can use the <b>UnRegisterForNotification</b> method to cancel previous requests for notifications.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>