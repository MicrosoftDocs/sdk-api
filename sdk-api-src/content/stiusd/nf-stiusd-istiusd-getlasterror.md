---
UID: NF:stiusd.IStiUSD.GetLastError
title: IStiUSD::GetLastError method
author: windows-driver-content
description: The IStiUSD::GetLastError method returns the last known error associated with a still image device.
old-location: image\istiusd_getlasterror.htm
old-project: image
ms.assetid: a7f265b8-c8a9-4a79-85e2-e3f52bf25f31
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetLastError method [Imaging Devices], GetLastError method [Imaging Devices], IStiUSD interface, GetLastError,IStiUSD.GetLastError, IStiUSD, IStiUSD interface [Imaging Devices], GetLastError method, IStiUSD::GetLastError, image.istiusd_getlasterror, stifnc_fad89b49-ff86-4a75-bae4-0aae22d9f5d6.xml, stiusd/IStiUSD::GetLastError
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
-	IStiUSD.GetLastError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD::GetLastError method


## -description


The <b>IStiUSD::GetLastError</b> method returns the last known error associated with a still image device.


## -parameters




### -param pdwLastDeviceError

Caller-supplied pointer to a buffer in which the error code will be stored.


## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543747">IStiDevice::GetLastError</a>



<a href="https://msdn.microsoft.com/62740263-5bbb-48e1-be3d-9ee9cb37d6b9">IStiUSD</a>
 

 

