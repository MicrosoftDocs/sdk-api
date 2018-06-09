---
UID: NF:mbnapi.IMbnConnectionManagerEvents.OnConnectionArrival
title: IMbnConnectionManagerEvents::OnConnectionArrival
author: windows-sdk-content
description: Notification method that indicates a new connection was added to the system.
old-location: mbn\imbnconnectionmanagerevents_onconnectionarrival.htm
old-project: mbn
ms.assetid: 88e48ce0-b2eb-431e-be0f-03b1d22ca61b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],OnConnectionArrival method, IMbnConnectionManagerEvents.OnConnectionArrival, IMbnConnectionManagerEvents::OnConnectionArrival, OnConnectionArrival, OnConnectionArrival method [Microsoft Broadband Networks], OnConnectionArrival method [Microsoft Broadband Networks],IMbnConnectionManagerEvents interface, mbn.imbnconnectionmanagerevents_onconnectionarrival, mbnapi/IMbnConnectionManagerEvents::OnConnectionArrival
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
 - IMbnConnectionManagerEvents.OnConnectionArrival
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionManagerEvents::OnConnectionArrival


## -description


Notification method that indicates a new connection was added to the system.


## -parameters




### -param newConnection [in]

An <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the device added to the system.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/153ab8c5-2b39-44a7-8c12-9f1df0012270">IMbnConnectionManagerEvents</a>
 

 

