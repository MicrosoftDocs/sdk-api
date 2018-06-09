---
UID: NF:mbnapi.IMbnInterfaceEvents.OnEmergencyModeChange
title: IMbnInterfaceEvents::OnEmergencyModeChange
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate that the emergency mode has changed.
old-location: mbn\imbninterfaceevents_onemergencymodechange.htm
old-project: mbn
ms.assetid: 637e0f6b-102f-436c-b0ec-edef16245675
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnEmergencyModeChange method, IMbnInterfaceEvents.OnEmergencyModeChange, IMbnInterfaceEvents::OnEmergencyModeChange, OnEmergencyModeChange, OnEmergencyModeChange method [Microsoft Broadband Networks], OnEmergencyModeChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onemergencymodechange, mbnapi/IMbnInterfaceEvents::OnEmergencyModeChange
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
 - IMbnInterfaceEvents.OnEmergencyModeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnEmergencyModeChange


## -description


This notification method is called by the Mobile Broadband service to indicate that the emergency mode has changed.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the device whose emergency mode has changed.  


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can call the <a href="https://msdn.microsoft.com/b4ce2c10-627d-4cbe-a884-7bb8731c3bcf">InEmergencyMode</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get the new emergency mode of the device.




## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

