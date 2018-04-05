---
UID: NF:mbnapi.IMbnInterfaceEvents.OnPreferredProvidersChange
title: IMbnInterfaceEvents::OnPreferredProvidersChange method
author: windows-driver-content
description: This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.
old-location: mbn\imbninterfaceevents_onpreferredproviderschange.htm
old-project: mbn
ms.assetid: ccede3de-4dfd-469f-afb4-d1424c56c7bc
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnInterfaceEvents, IMbnInterfaceEvents interface [Microsoft Broadband Networks], OnPreferredProvidersChange method, IMbnInterfaceEvents::OnPreferredProvidersChange, OnPreferredProvidersChange method [Microsoft Broadband Networks], OnPreferredProvidersChange method [Microsoft Broadband Networks], IMbnInterfaceEvents interface, OnPreferredProvidersChange,IMbnInterfaceEvents.OnPreferredProvidersChange, mbn.imbninterfaceevents_onpreferredproviderschange, mbnapi/IMbnInterfaceEvents::OnPreferredProvidersChange
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
-	IMbnInterfaceEvents.OnPreferredProvidersChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnPreferredProvidersChange method


## -description


This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the Mobile Broadband device whose preferred provider list has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



In some cases, a device's preferred provider list can be updated by the network by SMS or OTA (over The air) update. The Mobile Broadband service will call this method to notify the application about any change in the preferred provider list. The application can call the <a href="https://msdn.microsoft.com/cbd37f0a-4245-415d-bd74-501aa4c7ade7">GetPreferredProviders</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get the updated list of preferred providers.


If there is a change in the preferred provider list because of a call to the <a href="https://msdn.microsoft.com/2ea95b4a-07d9-40d6-bb82-091b49c965c4">SetPreferredProviders</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>, then this notification will not be called. 













## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

