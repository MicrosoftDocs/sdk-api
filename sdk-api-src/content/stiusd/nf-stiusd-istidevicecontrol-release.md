---
UID: NF:stiusd.IStiDeviceControl.Release
title: IStiDeviceControl::Release method
author: windows-driver-content
description: The IStiDeviceControl::Release method closes the instance of the COM object that was created when a minidriver client called IStiUSD::Initialize.
old-location: image\istidevicecontrol_release.htm
old-project: image
ms.assetid: 56c2ddc0-9f25-4d4f-9f6e-d8c96c9acc91
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiDeviceControl, IStiDeviceControl interface [Imaging Devices], Release method, IStiDeviceControl::Release, Release method [Imaging Devices], Release method [Imaging Devices], IStiDeviceControl interface, Release,IStiDeviceControl.Release, image.istidevicecontrol_release, stifnc_c0e50ea5-46e3-4b30-92b4-be6906647671.xml, stiusd/IStiDeviceControl::Release
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
-	IStiDeviceControl.Release
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiDeviceControl::Release method


## -description


The <b>IStiDeviceControl::Release</b> method closes the instance of the COM object that was created when a minidriver client called <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a>.


## -parameters






## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>Stierr.h</i>.




## -remarks



The <b>IStiDeviceControl::Release</b> method should be called from within the destructor function of a user-mode still image minidriver's <b>IStiUSD</b> interface. (For more information, see <a href="https://msdn.microsoft.com/94fdbeba-5b4a-4b66-b381-ec362b6d38c9">Creating a User-Mode Still Image Minidriver</a>.)

A still image minidriver receives an <b>IStiDeviceControl</b> interface pointer as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.




## -see-also




<a href="https://msdn.microsoft.com/de58597a-d10a-45b3-bf75-539e5cd00535">IStiDeviceControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542933">IStiDeviceControl::AddRef</a>
 

 

