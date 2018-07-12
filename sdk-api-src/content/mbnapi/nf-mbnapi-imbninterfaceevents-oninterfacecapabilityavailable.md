---
UID: NF:mbnapi.IMbnInterfaceEvents.OnInterfaceCapabilityAvailable
title: IMbnInterfaceEvents::OnInterfaceCapabilityAvailable
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate that interface capability information is available.
old-location: mbn\imbninterfaceevents_oninterfacecapabilityavailable.htm
old-project: mbn
ms.assetid: eeeffe13-307b-45f3-aa24-c33c621aa18e
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnInterfaceCapabilityAvailable method, IMbnInterfaceEvents.OnInterfaceCapabilityAvailable, IMbnInterfaceEvents::OnInterfaceCapabilityAvailable, OnInterfaceCapabilityAvailable, OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks], OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_oninterfacecapabilityavailable, mbnapi/IMbnInterfaceEvents::OnInterfaceCapabilityAvailable
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
 - IMbnInterfaceEvents.OnInterfaceCapabilityAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnInterfaceCapabilityAvailable


## -description


This notification method is called by the Mobile Broadband service to indicate that interface capability information is available.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> whose capability information has become available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



The application can issue the <a href="https://msdn.microsoft.com/cfe8f638-ad17-4118-9c79-b7ebc81c726a">GetInterfaceCapability</a> method  of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get the available capability information. For a list of interface capabilities, see <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a>





## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

