---
UID: NF:mbnapi.IMbnInterfaceManagerEvents.OnInterfaceRemoval
title: IMbnInterfaceManagerEvents::OnInterfaceRemoval
author: windows-sdk-content
description: Notification method that signals that a device has been removed from the system.
old-location: mbn\imbninterfacemanagerevents_oninterfaceremoval.htm
old-project: mbn
ms.assetid: d7c96d35-20e1-46e2-82db-4b1fc03cdd22
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks],OnInterfaceRemoval method, IMbnInterfaceManagerEvents.OnInterfaceRemoval, IMbnInterfaceManagerEvents::OnInterfaceRemoval, OnInterfaceRemoval, OnInterfaceRemoval method [Microsoft Broadband Networks], OnInterfaceRemoval method [Microsoft Broadband Networks],IMbnInterfaceManagerEvents interface, mbn.imbninterfacemanagerevents_oninterfaceremoval, mbnapi/IMbnInterfaceManagerEvents::OnInterfaceRemoval
ms.prod: windows
ms.technology: windows-sdk
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
 - IMbnInterfaceManagerEvents.OnInterfaceRemoval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceManagerEvents::OnInterfaceRemoval


## -description


Notification method that signals that a device has been removed from the system.


## -parameters




### -param oldInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the device that was removed.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/1d421668-cbea-4457-bbc3-dad1b53a5d70">IMbnInterfaceManagerEvents</a>
 

 

