---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvWriteItemProperties
title: IWiaMiniDrv::drvWriteItemProperties method
author: windows-driver-content
description: The IWiaMiniDrv::drvWriteItemProperties method writes driver item properties to a WIA hardware device.
old-location: image\iwiaminidrv_drvwriteitemproperties.htm
old-project: image
ms.assetid: 350cb7f6-499f-4fbc-b5c0-6f4daf2a2af0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvWriteItemProperties method, IWiaMiniDrv::drvWriteItemProperties, MiniDrv_9296f23a-679c-48e0-b594-ece8a1030e50.xml, drvWriteItemProperties method [Imaging Devices], drvWriteItemProperties method [Imaging Devices], IWiaMiniDrv interface, drvWriteItemProperties,IWiaMiniDrv.drvWriteItemProperties, image.iwiaminidrv_drvwriteitemproperties, wiamindr_lh/IWiaMiniDrv::drvWriteItemProperties
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
-	IWiaMiniDrv.drvWriteItemProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvWriteItemProperties method


## -description


The <b>IWiaMiniDrv::drvWriteItemProperties</b> method writes driver item properties to a WIA hardware device.


## -parameters




### -param __MIDL__IWiaMiniDrv0021




### -param __MIDL__IWiaMiniDrv0022




### -param __MIDL__IWiaMiniDrv0023




### -param __MIDL__IWiaMiniDrv0024






#### - lFlags [in]

Is currently unused. 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


#### - pmdtc [in]

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure containing the device transfer context.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>.

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545005">IWiaMiniDrv::drvReadItemProperties</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549264">wiasGetRootItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549300">wiasReadMultiple</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549308">wiasReadPropBin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549320">wiasReadPropFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549325">wiasReadPropGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549330">wiasReadPropLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549341">wiasReadPropStr</a>
 

 

