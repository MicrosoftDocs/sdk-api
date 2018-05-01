---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvDeviceCommand
title: IWiaMiniDrv::drvDeviceCommand method
author: windows-driver-content
description: The IWiaMiniDrv::drvDeviceCommand method issues a command to a WIA device.
old-location: image\iwiaminidrv_drvdevicecommand.htm
old-project: image
ms.assetid: e17c81a6-8c4e-41f0-bd98-f7a9a0f20893
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvDeviceCommand method, IWiaMiniDrv::drvDeviceCommand, MiniDrv_a65ceaef-73bf-4fd1-9d56-2a4b208f54a3.xml, drvDeviceCommand method [Imaging Devices], drvDeviceCommand method [Imaging Devices], IWiaMiniDrv interface, drvDeviceCommand,IWiaMiniDrv.drvDeviceCommand, image.iwiaminidrv_drvdevicecommand, wiamindr_lh/IWiaMiniDrv::drvDeviceCommand
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
-	IWiaMiniDrv.drvDeviceCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvDeviceCommand method


## -description


The <b>IWiaMiniDrv::drvDeviceCommand</b> method issues a command to a WIA device.


## -parameters




### -param __MIDL__IWiaMiniDrv0043




### -param __MIDL__IWiaMiniDrv0044




### -param __MIDL__IWiaMiniDrv0045




### -param __MIDL__IWiaMiniDrv0046




### -param __MIDL__IWiaMiniDrv0047






#### - lFlags [in]

Is currently unused. 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plCommand [in]

Points to a WIA command GUID. 


#### - plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


#### - ppWiaDrvItem [out, optional]

Points to a memory location that can receive a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff543896">IWiaDrvItem Interface</a>. See Remarks.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>. 

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.






## -remarks



The method <b>IWiaMiniDrv::drvDeviceCommand</b> is called by the WIA service to issue a WIA service or application generated command to the device. The WIA service only calls the <b>IWiaMiniDrv::drvDeviceCommand </b>method for a command that the device can support in the method <a href="https://msdn.microsoft.com/library/windows/hardware/ff543977">IWiaMiniDrv::drvGetCapabilities</a>.

The <i>ppWiaDrvItem</i> parameter should be considered to be optional, since the minidriver does not normally set the memory location it points to. For certain commands, however, the minidriver places the address of a newly created item in the location pointed to by this parameter. For example, if the command to take a picture is issued (<i>plCommand</i> is set to WIA_CMD_TAKE_PICTURE), the device produces a new image, causing the minidriver to create a new item in the driver item tree, and sets *<i>ppWiaDrvItem</i> to the address of the new item. This informs the WIA service that a new item was created.

The minidriver may include a list of custom commands the device can support in the method <a href="https://msdn.microsoft.com/library/windows/hardware/ff543977">IWiaMiniDrv::drvGetCapabilities</a>.

The WIA service does not write any properties before calling this method. If the command relies on property settings, the minidriver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff545020">IWiaMiniDrv::drvWriteItemProperties</a> before issuing the command. For example, the command to take a picture, WIA_CMD_TAKE_PICTURE, might rely on shutter speed and aperture settings, which need to be written to the device before the command is issued.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543977">IWiaMiniDrv::drvGetCapabilities</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545020">IWiaMiniDrv::drvWriteItemProperties</a>
 

 

