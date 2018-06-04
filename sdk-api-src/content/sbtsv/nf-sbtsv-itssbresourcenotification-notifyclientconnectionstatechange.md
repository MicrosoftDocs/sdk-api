---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

A pointer to an <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> connection object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



RD Connection Broker calls the <b>NotifyClientConnectionStateChange</b> method to notify registered plug-ins about state changes in a client connection.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>
 

 

