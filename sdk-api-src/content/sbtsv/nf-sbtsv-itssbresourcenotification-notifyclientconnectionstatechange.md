---
UID: NF:sbtsv.ITsSbResourceNotification.NotifyClientConnectionStateChange
title: ITsSbResourceNotification::NotifyClientConnectionStateChange (sbtsv.h)
description: Notifies registered plug-ins about state changes in a client connection. (ITsSbResourceNotification.NotifyClientConnectionStateChange)
helpviewer_keywords: ["CONNECTION_REQUEST_CANCELLED","CONNECTION_REQUEST_FAILED","CONNECTION_REQUEST_PENDING","CONNECTION_REQUEST_SUCCEEDED","CONNECTION_REQUEST_TIMEDOUT","ITsSbResourceNotification interface [Remote Desktop Services]","NotifyClientConnectionStateChange method","ITsSbResourceNotification.NotifyClientConnectionStateChange","ITsSbResourceNotification::NotifyClientConnectionStateChange","NotifyClientConnectionStateChange","NotifyClientConnectionStateChange method [Remote Desktop Services]","NotifyClientConnectionStateChange method [Remote Desktop Services]","ITsSbResourceNotification interface","sbtsv/ITsSbResourceNotification::NotifyClientConnectionStateChange","termserv.itssbresourcenotification_notifyclientconnectionstatechange"]
old-location: termserv\itssbresourcenotification_notifyclientconnectionstatechange.htm
tech.root: TermServ
ms.assetid: 8c5d6cf4-f99c-46fa-8b8e-008ff8a4d0d7
ms.date: 12/05/2018
ms.keywords: CONNECTION_REQUEST_CANCELLED, CONNECTION_REQUEST_FAILED, CONNECTION_REQUEST_PENDING, CONNECTION_REQUEST_SUCCEEDED, CONNECTION_REQUEST_TIMEDOUT, ITsSbResourceNotification interface [Remote Desktop Services],NotifyClientConnectionStateChange method, ITsSbResourceNotification.NotifyClientConnectionStateChange, ITsSbResourceNotification::NotifyClientConnectionStateChange, NotifyClientConnectionStateChange, NotifyClientConnectionStateChange method [Remote Desktop Services], NotifyClientConnectionStateChange method [Remote Desktop Services],ITsSbResourceNotification interface, sbtsv/ITsSbResourceNotification::NotifyClientConnectionStateChange, termserv.itssbresourcenotification_notifyclientconnectionstatechange
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
 - ITsSbResourceNotification::NotifyClientConnectionStateChange
 - sbtsv/ITsSbResourceNotification::NotifyClientConnectionStateChange
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
 - ITsSbResourceNotification.NotifyClientConnectionStateChange
---

# ITsSbResourceNotification::NotifyClientConnectionStateChange


## -description

Notifies registered plug-ins about state changes in a client connection.

## -parameters

### -param ChangeType [in]

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

### -param pConnection [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> connection object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

RD Connection Broker calls the <b>NotifyClientConnectionStateChange</b> method to notify registered plug-ins about state changes in a client connection.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>
