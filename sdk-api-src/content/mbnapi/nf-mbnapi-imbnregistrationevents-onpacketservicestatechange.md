---
UID: NF:mbnapi.IMbnRegistrationEvents.OnPacketServiceStateChange
title: IMbnRegistrationEvents::OnPacketServiceStateChange
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate a change in the device packet service state.
old-location: mbn\imbnregistrationevents_onpacketservicestatechange.htm
old-project: mbn
ms.assetid: 19199009-a4ac-4bf9-adfc-46c06d861485
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnPacketServiceStateChange method, IMbnRegistrationEvents.OnPacketServiceStateChange, IMbnRegistrationEvents::OnPacketServiceStateChange, OnPacketServiceStateChange, OnPacketServiceStateChange method [Microsoft Broadband Networks], OnPacketServiceStateChange method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, mbn.imbnregistrationevents_onpacketservicestatechange, mbnapi/IMbnRegistrationEvents::OnPacketServiceStateChange
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnRegistrationEvents.OnPacketServiceStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistrationEvents::OnPacketServiceStateChange


## -description


Notification method called by the Mobile Broadband service to indicate a change in the device packet service state.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> interface that represents the device whose packet service state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



The <b>OnPacketServiceStateChange</b> method is called by the Mobile Broadband service to signal a change in the packet service state of the device. This can occur if	there is a change in the current data class, the available data class, or a packet attach network error.
An application can use the passed <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> interface to get updated state values.




## -see-also




<a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>
 

 

