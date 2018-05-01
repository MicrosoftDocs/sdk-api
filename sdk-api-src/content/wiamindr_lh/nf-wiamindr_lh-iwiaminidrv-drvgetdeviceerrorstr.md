---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvGetDeviceErrorStr
title: IWiaMiniDrv::drvGetDeviceErrorStr method
author: windows-driver-content
description: The IWiaMiniDrv::drvGetDeviceErrorStr method maps an error code to a Unicode string that describes the error.
old-location: image\iwiaminidrv_drvgetdeviceerrorstr.htm
old-project: image
ms.assetid: c34a6834-8875-400c-9634-6c2b9b68164f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvGetDeviceErrorStr method, IWiaMiniDrv::drvGetDeviceErrorStr, MiniDrv_d5a72b62-8987-4d0a-921e-8a7f4d915d12.xml, drvGetDeviceErrorStr method [Imaging Devices], drvGetDeviceErrorStr method [Imaging Devices], IWiaMiniDrv interface, drvGetDeviceErrorStr,IWiaMiniDrv.drvGetDeviceErrorStr, image.iwiaminidrv_drvgetdeviceerrorstr, wiamindr_lh/IWiaMiniDrv::drvGetDeviceErrorStr
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
-	IWiaMiniDrv.drvGetDeviceErrorStr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvGetDeviceErrorStr method


## -description


The <b>IWiaMiniDrv::drvGetDeviceErrorStr </b>method maps an error code to a Unicode string that describes the error.


## -parameters




### -param __MIDL__IWiaMiniDrv0039




### -param __MIDL__IWiaMiniDrv0040




### -param __MIDL__IWiaMiniDrv0041




### -param __MIDL__IWiaMiniDrv0042






#### - lDevErrVal [in]

Specifies the device error value to be mapped to a string. A value of zero indicates that no error occurred.


#### - lFlags [in]

Is currently unused. 


#### - plDevErr [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


#### - ppszDevErrStr [out, optional]

Points to a memory location that will receive the address of a string describing the error. 


## -returns



On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErr</i>. If the minidriver does not fully implement this method, the method should return E_NOTIMPL. If the minidriver does not recognize the error value passed to this method, the method should return E_INVALIDARG. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErr</i>.




## -remarks



To obtain an error string that describes a device-specific minidriver-generated error value, the WIA service calls the <b>IWiaMiniDrv::drvGetDeviceErrorStr</b> method. In response to this call, the minidriver should use <b>CoTaskMemAlloc</b> (described in the Microsoft Windows SDK documentation) to allocate memory that will contain a localized Unicode string corresponding to the error code passed to the minidriver. The WIA service (or an application) will free the memory. It is likely that an application will display the string, so it should be meaningful to an end user. The string should be loaded from a resource file, so that it can be localized into a variety of languages.



