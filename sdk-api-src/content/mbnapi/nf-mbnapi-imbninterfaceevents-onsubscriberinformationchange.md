---
UID: NF:mbnapi.IMbnInterfaceEvents.OnSubscriberInformationChange
title: IMbnInterfaceEvents::OnSubscriberInformationChange
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate that the subscriber information for the device has changed.
old-location: mbn\imbninterfaceevents_onsubscriberinformationchange.htm
old-project: mbn
ms.assetid: 26d4fbdb-9c13-4934-a6bb-df581d0c18e9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnSubscriberInformationChange method, IMbnInterfaceEvents.OnSubscriberInformationChange, IMbnInterfaceEvents::OnSubscriberInformationChange, OnSubscriberInformationChange, OnSubscriberInformationChange method [Microsoft Broadband Networks], OnSubscriberInformationChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onsubscriberinformationchange, mbnapi/IMbnInterfaceEvents::OnSubscriberInformationChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnInterfaceEvents.OnSubscriberInformationChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnSubscriberInformationChange


## -description


This notification method is called by the Mobile Broadband service to indicate that the subscriber information for the device has changed.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents a device on which the subscriber information has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



The application can call the <a href="https://msdn.microsoft.com/9114a3ed-2dc9-4637-b3d5-9430d309e89b">GetSubscriberInformation</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get new subscriber information.




## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

