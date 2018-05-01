---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvValidateItemProperties
title: IWiaMiniDrv::drvValidateItemProperties method
author: windows-driver-content
description: The IWiaMiniDrv::drvValidateItemProperties method validates an item's properties against the set of valid values for each property and will update those properties if necessary.
old-location: image\iwiaminidrv_drvvalidateitemproperties.htm
old-project: image
ms.assetid: 12052128-9ea7-41cd-bb75-be7175e26c12
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvValidateItemProperties method, IWiaMiniDrv::drvValidateItemProperties, MiniDrv_b288e05c-a142-452a-9ac7-ffb2dfcae4cf.xml, drvValidateItemProperties method [Imaging Devices], drvValidateItemProperties method [Imaging Devices], IWiaMiniDrv interface, drvValidateItemProperties,IWiaMiniDrv.drvValidateItemProperties, image.iwiaminidrv_drvvalidateitemproperties, wiamindr_lh/IWiaMiniDrv::drvValidateItemProperties
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
-	IWiaMiniDrv.drvValidateItemProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvValidateItemProperties method


## -description


The <b>IWiaMiniDrv::drvValidateItemProperties</b> method validates an item's properties against the set of valid values for each property and will update those properties if necessary.


## -parameters




### -param __MIDL__IWiaMiniDrv0016




### -param __MIDL__IWiaMiniDrv0017




### -param __MIDL__IWiaMiniDrv0018




### -param __MIDL__IWiaMiniDrv0019




### -param __MIDL__IWiaMiniDrv0020






#### - lFlags [in]

Is reserved. Set to zero. 


#### - nPropSpec [in]

Indicates the number of items n the <i>pPropSpec</i> array.


#### - pPropSpec [in]

Points to the first element of an array of PROPSPEC structures (defined in the Microsoft Windows SDK documentation). 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>.

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549255">wiasGetItemType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549454">wiasValidateItemProperties</a>
 

 

