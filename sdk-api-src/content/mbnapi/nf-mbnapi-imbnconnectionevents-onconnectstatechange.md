---
UID: NF:mbnapi.IMbnConnectionEvents.OnConnectStateChange
title: IMbnConnectionEvents::OnConnectStateChange (mbnapi.h)
author: windows-sdk-content
description: Notification method that indicates whether the connection state of the device has changed.
old-location: mbn\imbnconnectionevents_onconnectstatechange.htm
tech.root: mbn
ms.assetid: 5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnConnectStateChange method, IMbnConnectionEvents.OnConnectStateChange, IMbnConnectionEvents::OnConnectStateChange, OnConnectStateChange, OnConnectStateChange method [Microsoft Broadband Networks], OnConnectStateChange method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_onconnectstatechange, mbnapi/IMbnConnectionEvents::OnConnectStateChange
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionEvents.OnConnectStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionEvents::OnConnectStateChange


## -description


Notification method that indicates whether the connection state of the device has changed.


## -parameters




### -param newConnection [in]

An <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the connection on which the state has changed due to a system or network initiated change.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> to get the updated connection state. 




## -see-also




<a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>
 

 

