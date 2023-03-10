---
UID: NF:sbtsv.ITsSbResourceNotificationEx.NotifyClientConnectionStateChangeEx
title: ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx (sbtsv.h)
description: Notifies registered plug-ins about state changes in a client connection. (ITsSbResourceNotificationEx.NotifyClientConnectionStateChangeEx)
helpviewer_keywords: ["CONNECTION_REQUEST_CANCELLED","CONNECTION_REQUEST_FAILED","CONNECTION_REQUEST_PENDING","CONNECTION_REQUEST_SUCCEEDED","CONNECTION_REQUEST_TIMEDOUT","ITsSbResourceNotificationEx interface [Remote Desktop Services]","NotifyClientConnectionStateChangeEx method","ITsSbResourceNotificationEx.NotifyClientConnectionStateChangeEx","ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx","NotifyClientConnectionStateChangeEx","NotifyClientConnectionStateChangeEx method [Remote Desktop Services]","NotifyClientConnectionStateChangeEx method [Remote Desktop Services]","ITsSbResourceNotificationEx interface","sbtsv/ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx","termserv.itssbresourcenotificationex_notifyclientconnectionstatechangeex"]
old-location: termserv\itssbresourcenotificationex_notifyclientconnectionstatechangeex.htm
tech.root: TermServ
ms.assetid: 79f59e18-f9ca-4e64-b8a1-8b0dd2b2715e
ms.date: 12/05/2018
ms.keywords: CONNECTION_REQUEST_CANCELLED, CONNECTION_REQUEST_FAILED, CONNECTION_REQUEST_PENDING, CONNECTION_REQUEST_SUCCEEDED, CONNECTION_REQUEST_TIMEDOUT, ITsSbResourceNotificationEx interface [Remote Desktop Services],NotifyClientConnectionStateChangeEx method, ITsSbResourceNotificationEx.NotifyClientConnectionStateChangeEx, ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx, NotifyClientConnectionStateChangeEx, NotifyClientConnectionStateChangeEx method [Remote Desktop Services], NotifyClientConnectionStateChangeEx method [Remote Desktop Services],ITsSbResourceNotificationEx interface, sbtsv/ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx, termserv.itssbresourcenotificationex_notifyclientconnectionstatechangeex
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
 - ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx
 - sbtsv/ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx
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
 - ITsSbResourceNotificationEx.NotifyClientConnectionStateChangeEx
---

# ITsSbResourceNotificationEx::NotifyClientConnectionStateChangeEx


## -description

Notifies registered plug-ins about state changes in a client connection.

## -parameters

### -param userName [in]

The user name.

### -param domain [in]

The user domain.

### -param initialProgram [in]

The initial program.

### -param poolName [in]

The name of the pool.

### -param targetName [in]

The name of the target.

### -param connectionChangeType [in]

The type of change that has occurred. This parameter can be one of the following values.



#### CONNECTION_REQUEST_PENDING

A client request is pending a session logon 
from 
a 
user.



#### CONNECTION_REQUEST_FAILED

RD Connection Broker failed to process the request. 
This value is 
issued just before 
RD Connection Broker deletes the connection request from its store.



#### CONNECTION_REQUEST_TIMEDOUT

The 
request timed out. This generally means 
that either the user has canceled the request or was unable to log on 
because of network connectivity issues. This value is 
issued just before 
RD Connection Broker deletes the connection request from its store.



#### CONNECTION_REQUEST_SUCCEEDED

The user successfully logged on to the target computer. This 
value is issued just before 
RD Connection Broker deletes the connection request from its store.



#### CONNECTION_REQUEST_CANCELLED

RD Connection Broker 
canceled a connection request

 because the
 connection 
request was being processed while the 
RD Connection Broker service was stopping.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex">ITsSbResourceNotificationEx</a>
