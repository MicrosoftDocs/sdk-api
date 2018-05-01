---
UID: NF:stiusd.IStiUSD.LockDevice
title: IStiUSD::LockDevice method
author: windows-driver-content
description: A still image minidriver's IStiUSD::LockDevice method locks a device for exclusive use by the caller.
old-location: image\istiusd_lockdevice.htm
old-project: image
ms.assetid: cb91ef14-53d7-42fa-b3e5-54eb3b0925b8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiUSD, IStiUSD interface [Imaging Devices], LockDevice method, IStiUSD::LockDevice, LockDevice method [Imaging Devices], LockDevice method [Imaging Devices], IStiUSD interface, LockDevice,IStiUSD.LockDevice, image.istiusd_lockdevice, stifnc_147be8d0-9e2a-4ade-99ce-36c7f3a8adeb.xml, stiusd/IStiUSD::LockDevice
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
-	Stiusd.h
api_name:
-	IStiUSD.LockDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD::LockDevice method


## -description


A still image minidriver's <b>IStiUSD::LockDevice</b> method locks a device for exclusive use by the caller.


## -parameters






## -returns



If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



If you are writing a driver for a device connected to a serial port, you might want to call <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> from within the driver's <b>IStiUSD::LockDevice</b> method if the device was opened in status mode. This will prohibit other applications from using the port (which might be supporting other devices) while status information is being obtained. For more information, see <a href="https://msdn.microsoft.com/79af0d8f-dd04-4ff4-a047-f415562a16a5">Transfer Modes</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543756">IStiDevice::LockDevice</a>



<a href="https://msdn.microsoft.com/62740263-5bbb-48e1-be3d-9ee9cb37d6b9">IStiUSD</a>
 

 

