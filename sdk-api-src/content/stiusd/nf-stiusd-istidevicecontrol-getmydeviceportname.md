---
UID: NF:stiusd.IStiDeviceControl.GetMyDevicePortName
title: IStiDeviceControl::GetMyDevicePortName method
author: windows-driver-content
description: The IStiDeviceControl::GetMyDevicePortName method allows a user-mode still image minidriver to obtain a device's port name.
old-location: image\istidevicecontrol_getmydeviceportname.htm
old-project: image
ms.assetid: f400ab05-aea9-4154-a725-5b23a6dc06b6
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetMyDevicePortName method [Imaging Devices], GetMyDevicePortName method [Imaging Devices], IStiDeviceControl interface, GetMyDevicePortName,IStiDeviceControl.GetMyDevicePortName, IStiDeviceControl, IStiDeviceControl interface [Imaging Devices], GetMyDevicePortName method, IStiDeviceControl::GetMyDevicePortName, image.istidevicecontrol_getmydeviceportname, stifnc_00f6a8a0-b5dc-43d7-8a68-23b15592b404.xml, stiusd/IStiDeviceControl::GetMyDevicePortName
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
-	IStiDeviceControl.GetMyDevicePortName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiDeviceControl::GetMyDevicePortName method


## -description


The <b>IStiDeviceControl::GetMyDevicePortName</b> method allows a user-mode still image minidriver to obtain a device's port name.


## -parameters




### -param lpszDevicePath

Caller-supplied pointer to a buffer to receive the device's port name.


### -param cwDevicePathSize

Caller-supplied number of characters (of type TCHAR) in the buffer pointed to by <i>lpszDevicePath</i>.


## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



The path name that a still image minidriver receives by calling <b>IStiDeviceControl::GetMyDevicePortName</b> can be used as an input argument to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> (described in the Microsoft Windows SDK documentation).

A still image minidriver receives an <b>IStiDeviceControl</b> interface pointer as an input argument to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.



