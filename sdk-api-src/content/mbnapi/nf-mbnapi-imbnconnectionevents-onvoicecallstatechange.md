---
UID: NF:mbnapi.IMbnConnectionEvents.OnVoiceCallStateChange
title: IMbnConnectionEvents::OnVoiceCallStateChange
author: windows-driver-content
description: Notification method that indicates a change in the voice call state of a device.
old-location: mbn\imbnconnectionevents_onvoicecallstatechange.htm
old-project: mbn
ms.assetid: c4f243b0-e6d5-4afc-85ad-0f88140c3beb
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnVoiceCallStateChange method, IMbnConnectionEvents.OnVoiceCallStateChange, IMbnConnectionEvents::OnVoiceCallStateChange, OnVoiceCallStateChange, OnVoiceCallStateChange method [Microsoft Broadband Networks], OnVoiceCallStateChange method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_onvoicecallstatechange, mbnapi/IMbnConnectionEvents::OnVoiceCallStateChange
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
-	IMbnConnectionEvents.OnVoiceCallStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionEvents::OnVoiceCallStateChange


## -description


Notification method that indicates a change in the voice call state of a device.


## -parameters




### -param newConnection [in]

An <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interface that represents the connection for which the voice call state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



<b>OnVoiceCallStateChange</b> is called when voice call state is available or when there is a change in the voice call state.   An application can use <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> to get the updated voice call state.




## -see-also




<a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>
 

 

