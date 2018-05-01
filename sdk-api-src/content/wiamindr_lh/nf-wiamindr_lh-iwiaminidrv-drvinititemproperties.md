---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvInitItemProperties
title: IWiaMiniDrv::drvInitItemProperties method
author: windows-driver-content
description: The IWiaMiniDrv::drvInitItemProperties method initializes WIA driver item properties for each item in an application item tree.
old-location: image\iwiaminidrv_drvinititemproperties.htm
old-project: image
ms.assetid: 06dce5c0-f893-47c7-bee9-1b7f61137ba0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvInitItemProperties method, IWiaMiniDrv::drvInitItemProperties, MiniDrv_88720847-db1d-475a-b8c4-62fdb376953a.xml, drvInitItemProperties method [Imaging Devices], drvInitItemProperties method [Imaging Devices], IWiaMiniDrv interface, drvInitItemProperties,IWiaMiniDrv.drvInitItemProperties, image.iwiaminidrv_drvinititemproperties, wiamindr_lh/IWiaMiniDrv::drvInitItemProperties
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
-	IWiaMiniDrv.drvInitItemProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvInitItemProperties method


## -description


The<b> IWiaMiniDrv::drvInitItemProperties</b> method initializes WIA driver item properties for each item in an application item tree.


## -parameters




### -param __MIDL__IWiaMiniDrv0013




### -param __MIDL__IWiaMiniDrv0014




### -param __MIDL__IWiaMiniDrv0015






#### - lFlags [in]

Is reserved. Set to zero. 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>. 

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.




## -remarks



The <b>IWiaMiniDrv::drvInitItemProperties</b> method is called once per application for each item in the item tree.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549243">wiasGetDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549358">wiasSetItemPropAttribs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549369">wiasSetItemPropNames</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549475">wiasWriteMultiple</a>
 

 

