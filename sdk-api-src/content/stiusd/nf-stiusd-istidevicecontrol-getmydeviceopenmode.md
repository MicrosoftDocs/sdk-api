---
UID: NF:stiusd.IStiDeviceControl.GetMyDeviceOpenMode
title: IStiDeviceControl::GetMyDeviceOpenMode method
author: windows-driver-content
description: The IStiDeviceControl::GetMyDeviceOpenMode method allows a still image minidriver to obtain the transfer mode that an application specified when it created an instance of a still image device.
old-location: image\istidevicecontrol_getmydeviceopenmode.htm
old-project: image
ms.assetid: 814e739f-6147-4287-876e-db6fc41c5aa1
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetMyDeviceOpenMode method [Imaging Devices], GetMyDeviceOpenMode method [Imaging Devices], IStiDeviceControl interface, GetMyDeviceOpenMode,IStiDeviceControl.GetMyDeviceOpenMode, IStiDeviceControl, IStiDeviceControl interface [Imaging Devices], GetMyDeviceOpenMode method, IStiDeviceControl::GetMyDeviceOpenMode, image.istidevicecontrol_getmydeviceopenmode, stifnc_a3082d9f-d152-4494-b11f-e9d2bd1efe63.xml, stiusd/IStiDeviceControl::GetMyDeviceOpenMode
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
-	stiusd.h
api_name:
-	IStiDeviceControl.GetMyDeviceOpenMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiDeviceControl::GetMyDeviceOpenMode method


## -description


The <b>IStiDeviceControl::GetMyDeviceOpenMode</b> method allows a still image minidriver to obtain the transfer mode that an application specified when it created an instance of a still image device.


## -parameters




### -param pdwOpenMode

Receives the mode flag that an application previously specified as the <i>dwMode</i> argument to <a href="https://msdn.microsoft.com/library/windows/hardware/ff543778">IStillImage::CreateDevice</a>.


## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



A still image minidriver receives an <b>IStiDeviceControl</b> interface pointer as an input argument to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.



