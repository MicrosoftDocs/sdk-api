---
UID: NF:mbnapi.IMbnConnectionManagerEvents.OnConnectionRemoval
title: IMbnConnectionManagerEvents::OnConnectionRemoval
author: windows-sdk-content
description: Notification method that indicates a connection was removed from the system.
old-location: mbn\imbnconnectionmanagerevents_onconnectionremoval.htm
tech.root: mbn
ms.assetid: 020ee1ad-cab5-4a27-b97b-160319d84ac8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],OnConnectionRemoval method, IMbnConnectionManagerEvents.OnConnectionRemoval, IMbnConnectionManagerEvents::OnConnectionRemoval, OnConnectionRemoval, OnConnectionRemoval method [Microsoft Broadband Networks], OnConnectionRemoval method [Microsoft Broadband Networks],IMbnConnectionManagerEvents interface, mbn.imbnconnectionmanagerevents_onconnectionremoval, mbnapi/IMbnConnectionManagerEvents::OnConnectionRemoval
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMbnConnectionManagerEvents.OnConnectionRemoval
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionManagerEvents::OnConnectionRemoval


## -description


Notification method that indicates a connection was removed from the system.


## -parameters




### -param oldConnection [in]

An <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the device removed from the system.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/153ab8c5-2b39-44a7-8c12-9f1df0012270">IMbnConnectionManagerEvents</a>
 

 

