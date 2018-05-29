---
UID: NF:mbnapi.IMbnRegistrationEvents.OnRegisterModeAvailable
title: IMbnRegistrationEvents::OnRegisterModeAvailable
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that registration mode information is available.
old-location: mbn\imbnregistrationevents_onregistermodeavailable.htm
old-project: mbn
ms.assetid: 5c916f16-e8f5-4c8a-942c-3a9ae11905a7
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnRegisterModeAvailable method, IMbnRegistrationEvents.OnRegisterModeAvailable, IMbnRegistrationEvents::OnRegisterModeAvailable, OnRegisterModeAvailable, OnRegisterModeAvailable method [Microsoft Broadband Networks], OnRegisterModeAvailable method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, mbn.imbnregistrationevents_onregistermodeavailable, mbnapi/IMbnRegistrationEvents::OnRegisterModeAvailable
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
-	IMbnRegistrationEvents.OnRegisterModeAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistrationEvents::OnRegisterModeAvailable


## -description


Notification method called by the Mobile Broadband service to indicate that registration mode information is available.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> interface that represents the applicable device.


## -returns



This method must return <b>S_OK</b>.




## -remarks



The <b>OnRegisterModeAvailable</b> method is called by the Mobile Broadband service to signal that  the registration mode information for a device is available. An application can call the <a href="https://msdn.microsoft.com/30030eb8-3b08-4583-a7ba-0560db32007f">GetRegisterMode</a> method of the passed <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> get the current registration mode of the device.




## -see-also




<a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>
 

 

