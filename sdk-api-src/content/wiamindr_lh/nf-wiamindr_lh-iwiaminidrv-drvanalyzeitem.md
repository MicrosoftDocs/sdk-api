---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvAnalyzeItem
title: IWiaMiniDrv::drvAnalyzeItem method
author: windows-driver-content
description: The IWiaMiniDrv::drvAnalyzeItem method inspects an item, and creates subitems, if necessary.
old-location: image\iwiaminidrv_drvanalyzeitem.htm
old-project: image
ms.assetid: e742f898-e663-431d-870e-bb0fe7e89b5a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvAnalyzeItem method, IWiaMiniDrv::drvAnalyzeItem, MiniDrv_dfa93eeb-ea39-44b6-b465-5bff0f056763.xml, drvAnalyzeItem method [Imaging Devices], drvAnalyzeItem method [Imaging Devices], IWiaMiniDrv interface, drvAnalyzeItem,IWiaMiniDrv.drvAnalyzeItem, image.iwiaminidrv_drvanalyzeitem, wiamindr_lh/IWiaMiniDrv::drvAnalyzeItem
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
-	IWiaMiniDrv.drvAnalyzeItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvAnalyzeItem method


## -description


The <b>IWiaMiniDrv::drvAnalyzeItem</b> method inspects an item, and creates subitems, if necessary.


## -parameters




### -param __MIDL__IWiaMiniDrv0036




### -param __MIDL__IWiaMiniDrv0037




### -param __MIDL__IWiaMiniDrv0038






#### - lFlags [in]

Is currently unused. 


#### - pWiasContext [in]

Pointer to a WIA item context.


#### - plDevErrVal [in]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method is not fully implemented, it can return E_NOTIMPL. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>. 

The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>
 

 

