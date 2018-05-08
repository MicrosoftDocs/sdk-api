---
UID: NF:mbnapi.IMbnInterfaceEvents.OnReadyStateChange
title: IMbnInterfaceEvents::OnReadyStateChange
author: windows-driver-content
description: This notification method is called by the Mobile Broadband service to indicate a change in an interface's ready state.
old-location: mbn\imbninterfaceevents_onreadystatechange.htm
old-project: mbn
ms.assetid: eb4364b8-cbbf-44c7-ae13-66950ce614e9
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnReadyStateChange method, IMbnInterfaceEvents.OnReadyStateChange, IMbnInterfaceEvents::OnReadyStateChange, OnReadyStateChange, OnReadyStateChange method [Microsoft Broadband Networks], OnReadyStateChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onreadystatechange, mbnapi/IMbnInterfaceEvents::OnReadyStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnInterfaceEvents.OnReadyStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnReadyStateChange


## -description


This notification method is called by the Mobile Broadband service to indicate a change in an interface's ready state.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the Mobile Broadband device whose ready state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can call the <a href="https://msdn.microsoft.com/4236fd9d-292a-4840-b52e-c28c3e6eea10">GetReadyState</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get latest ready state of the device. For a list of ready states, see  <a href="https://msdn.microsoft.com/4f712cdc-ee9c-4ceb-9bc4-8a4fe19d0a37">MBN_READY_STATE</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

