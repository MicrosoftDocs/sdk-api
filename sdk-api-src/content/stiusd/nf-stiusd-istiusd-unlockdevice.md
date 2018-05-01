---
UID: NF:stiusd.IStiUSD.UnLockDevice
title: IStiUSD::UnLockDevice method
author: windows-driver-content
description: A still image minidriver's IStiUSD::UnLockDevice method unlocks a device that was locked by a previous call to IStiUSD::LockDevice.
old-location: image\istiusd_unlockdevice.htm
old-project: image
ms.assetid: ae19ae38-3bca-42c8-8713-68bb161104b8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiUSD, IStiUSD interface [Imaging Devices], UnLockDevice method, IStiUSD::UnLockDevice, UnLockDevice method [Imaging Devices], UnLockDevice method [Imaging Devices], IStiUSD interface, UnLockDevice,IStiUSD.UnLockDevice, image.istiusd_unlockdevice, stifnc_8c11e0a0-68ec-4556-ae40-6bed6b5b4831.xml, stiusd/IStiUSD::UnLockDevice
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
-	IStiUSD.UnLockDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD::UnLockDevice method


## -description


A still image minidriver's <b>IStiUSD::UnLockDevice</b> method unlocks a device that was locked by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff543829">IStiUSD::LockDevice</a>.


## -parameters






## -returns



If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



If a driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff543829">IStiUSD::LockDevice</a> method called <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>, then <b>IStiUSD::UnlockDevice</b> should call <b>CloseHandle</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543770">IStiDevice::UnLockDevice</a>



<a href="https://msdn.microsoft.com/62740263-5bbb-48e1-be3d-9ee9cb37d6b9">IStiUSD</a>
 

 

