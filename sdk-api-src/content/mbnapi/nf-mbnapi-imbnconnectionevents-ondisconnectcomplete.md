---
UID: NF:mbnapi.IMbnConnectionEvents.OnDisconnectComplete
title: IMbnConnectionEvents::OnDisconnectComplete
author: windows-sdk-content
description: Notification method that indicates that a disconnection operation has been performed.
old-location: mbn\imbnconnectionevents_ondisconnectcomplete.htm
old-project: mbn
ms.assetid: 2d225823-2b9b-4c3a-b847-7b2b9a13d121
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnDisconnectComplete method, IMbnConnectionEvents.OnDisconnectComplete, IMbnConnectionEvents::OnDisconnectComplete, OnDisconnectComplete, OnDisconnectComplete method [Microsoft Broadband Networks], OnDisconnectComplete method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_ondisconnectcomplete, mbnapi/IMbnConnectionEvents::OnDisconnectComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionEvents.OnDisconnectComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionEvents::OnDisconnectComplete


## -description


Notification method that indicates that a disconnection operation has been performed.


## -parameters




### -param newConnection [in]

An <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the connection that has been disconnected.


### -param requestID [in]

The request ID assigned by the Mobile Broadband service to identify the disconnection operation.


### -param status [in]

The operation completion status.  This can only be <b>S_OK</b>.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> to get the current connection state.  




## -see-also




<a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>
 

 

