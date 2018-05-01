---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvLockWiaDevice
title: IWiaMiniDrv::drvLockWiaDevice method
author: windows-driver-content
description: The IWiaMiniDrv::drvLockWiaDevice method locks the WIA hardware device so that only the current minidriver can access it.
old-location: image\iwiaminidrv_drvlockwiadevice.htm
old-project: image
ms.assetid: 674e0a65-1763-41b0-896b-2ef9debc32a5
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvLockWiaDevice method, IWiaMiniDrv::drvLockWiaDevice, MiniDrv_5ae2a5c5-524c-46ce-8ae4-d8edd5d76fcc.xml, drvLockWiaDevice method [Imaging Devices], drvLockWiaDevice method [Imaging Devices], IWiaMiniDrv interface, drvLockWiaDevice,IWiaMiniDrv.drvLockWiaDevice, image.iwiaminidrv_drvlockwiadevice, wiamindr_lh/IWiaMiniDrv::drvLockWiaDevice
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
-	IWiaMiniDrv.drvLockWiaDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvLockWiaDevice method


## -description


The <b>IWiaMiniDrv::drvLockWiaDevice</b> method locks the WIA hardware device so that only the current minidriver can access it.


## -parameters




### -param __MIDL__IWiaMiniDrv0030




### -param __MIDL__IWiaMiniDrv0031




### -param __MIDL__IWiaMiniDrv0032






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



The <b>IWiaMiniDrv::drvLockWiaDevice</b> method is used to lock access to the device. This is typically done before properties are written to the device or before a data transfer. The <b>IWiaMiniDrv::drvLockWiaDevice </b>method should be implemented using the <b>IStiDevice</b> interface's lock device method, <a href="https://msdn.microsoft.com/library/windows/hardware/ff543756">IStiDevice::LockDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545012">IWiaMiniDrv::drvUnLockWiaDevice</a>
 

 

