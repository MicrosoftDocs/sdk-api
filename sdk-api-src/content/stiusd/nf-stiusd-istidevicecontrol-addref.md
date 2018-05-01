---
UID: NF:stiusd.IStiDeviceControl.AddRef
title: IStiDeviceControl::AddRef method
author: windows-driver-content
description: The IStiDeviceControl::AddRef method increments the reference count for the IStiDeviceControl interface.
old-location: image\istidevicecontrol_addref.htm
old-project: image
ms.assetid: 8aa28efb-a030-4fed-b9f2-0e67ff1e7c9e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: AddRef method [Imaging Devices], AddRef method [Imaging Devices], IStiDeviceControl interface, AddRef,IStiDeviceControl.AddRef, IStiDeviceControl, IStiDeviceControl interface [Imaging Devices], AddRef method, IStiDeviceControl::AddRef, image.istidevicecontrol_addref, stifnc_b0cd1dfe-9e37-42a5-83e0-d0f97c9439e8.xml, stiusd/IStiDeviceControl::AddRef
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Stiusd.h
api_name:
-	IStiDeviceControl.AddRef
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiDeviceControl::AddRef method


## -description


The <b>IStiDeviceControl::AddRef</b> method increments the reference count for the <b>IStiDeviceControl</b> interface.


## -parameters






## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



The <b>IStiDeviceControl::AddRef</b> method should be called from within a user-mode still image minidriver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.

A still image minidriver receives an <b>IStiDeviceControl</b> interface pointer as an input argument to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.




## -see-also




<a href="https://msdn.microsoft.com/de58597a-d10a-45b3-bf75-539e5cd00535">IStiDeviceControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543725">IStiDeviceControl::Release</a>
 

 

