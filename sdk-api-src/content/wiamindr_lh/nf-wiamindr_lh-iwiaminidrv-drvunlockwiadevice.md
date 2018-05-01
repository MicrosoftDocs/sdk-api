---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvUnLockWiaDevice
title: IWiaMiniDrv::drvUnLockWiaDevice method
author: windows-driver-content
description: The IWiaMiniDrv::drvUnLockWiaDevice method unlocks the WIA hardware device so that any minidriver can access it.
old-location: image\iwiaminidrv_drvunlockwiadevice.htm
old-project: image
ms.assetid: 134d224a-d472-4d74-be3e-069dbb46a65c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvUnLockWiaDevice method, IWiaMiniDrv::drvUnLockWiaDevice, MiniDrv_596d3499-1e4a-4147-838f-db4f56f30716.xml, drvUnLockWiaDevice method [Imaging Devices], drvUnLockWiaDevice method [Imaging Devices], IWiaMiniDrv interface, drvUnLockWiaDevice,IWiaMiniDrv.drvUnLockWiaDevice, image.iwiaminidrv_drvunlockwiadevice, wiamindr_lh/IWiaMiniDrv::drvUnLockWiaDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later.
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
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiamindr_lh.h
api_name:
-	IWiaMiniDrv.drvUnLockWiaDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvUnLockWiaDevice method


## -description


The <b>IWiaMiniDrv::drvUnLockWiaDevice</b> method unlocks the WIA hardware device so that any minidriver can access it.


## -parameters




### -param __MIDL__IWiaMiniDrv0033




### -param __MIDL__IWiaMiniDrv0034




### -param __MIDL__IWiaMiniDrv0035






#### - lFlags [in]

Is currently unused. 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>.

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.




## -remarks



The method <b>IWiaMiniDrv::drvUnLockWiaDevice</b> is used to allow access to the device after the lock is no longer needed. It is typically called by the WIA service after properties are written to the device or after a data transfer. 

The minidriver's implementation of the <b>IWiaMiniDrv::drvUnLockWiaDevice</b> method should use the STI unlock device method <a href="https://msdn.microsoft.com/library/windows/hardware/ff543770">IStiDevice::UnLockDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544995">IWiaMiniDrv::drvLockWiaDevice</a>
 

 

