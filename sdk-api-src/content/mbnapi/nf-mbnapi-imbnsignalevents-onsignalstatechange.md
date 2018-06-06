---
UID: NF:mbnapi.IMbnSignalEvents.OnSignalStateChange
title: IMbnSignalEvents::OnSignalStateChange
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available.
old-location: mbn\imbnsignalevents_onsignalstatechange.htm
old-project: mbn
ms.assetid: 07e98555-03fa-4852-af65-55778dc9c477
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnSignalEvents interface [Microsoft Broadband Networks],OnSignalStateChange method, IMbnSignalEvents.OnSignalStateChange, IMbnSignalEvents::OnSignalStateChange, OnSignalStateChange, OnSignalStateChange method [Microsoft Broadband Networks], OnSignalStateChange method [Microsoft Broadband Networks],IMbnSignalEvents interface, mbn.imbnsignalevents_onsignalstatechange, mbnapi/IMbnSignalEvents::OnSignalStateChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnSignalEvents.OnSignalStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSignalEvents::OnSignalStateChange


## -description


This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/2b60d078-ccbd-4cc5-addf-e6e95832b3a1">IMbnSignal</a> interface  for which the signal quality update was received.


## -returns



This method must return <b>S_OK</b>.




## -remarks



<b>OnSignalStateChange</b> is called by the Mobile Broadband service to notify a calling application that a signal quality update is available.  This includes an update of the signal notification period, threshold for signal notification, signal strength received, and error rate in the received signal. 
An application can get updated values from the <a href="https://msdn.microsoft.com/2b60d078-ccbd-4cc5-addf-e6e95832b3a1">IMbnSignal</a> interface passed in this method.





## -see-also




<a href="https://msdn.microsoft.com/9e52168a-c6f9-4154-b8b9-8ae6cb771d46">IMbnSignalEvents</a>
 

 

